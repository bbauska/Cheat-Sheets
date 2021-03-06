# MySQL Cheat Sheet

## <a id="toc"></a>TOC

  - [General](#general)
  - [Users, privileges](#users-privileges)
  - [Table structure](#table-structure)
  - [Relations](#relations)
  - [Misc](#misc)
  - [Resources](#resources)

----

## <a id="general"></a>General

Host value examples: `localhost`, `%`, `127.0.0.1`, `%.example.com`, `192.168.1.%`, `192.168.1.0/255.255.255.0`.

#### Create database

```sql
CREATE DATABASE `<database>` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
```

## <a id="users-privileges"></a>Users, privileges

#### List users

```sql
SELECT `User`, `Host` FROM `mysql`.`user`;
```

#### Add a user

```sql
CREATE USER '<user>'@'<host>' IDENTIFIED BY '<pass>';
```

#### Remove a user

As of MySQL 5.1+ it will remove privileges as well.

```sql
DROP USER '<user>'@<host>;
```

#### Show privileges

```sql
SHOW GRANTS FOR '<user>'@'<host>';
```

#### Grant privileges

```sql
GRANT SELECT, INSERT, UPDATE, DELETE ON <database>.* TO '<user>'@'<host>';
FLUSH PRIVILEGES;
```

#### Revoke privileges

```sql
REVOKE INSERT, UPDATE, DELETE ON <database>.* FROM '<user>'@'<host>';
FLUSH PRIVILEGES;
```

#### Privileges list

  * **data**: SELECT, INSERT, UPDATE, DELETE, FILE
  * **structure**: CREATE, ALTER, INDEX, DROP, CREATE TEMPORARY TABLES, SHOW VIEW, CREATE ROUTINE, ALTER ROUTINE, EXECUTE, CREATE VIEW, EVENT, TRIGGER
  * **administration**: GRANT, SUPER, PROCESS, RELOAD, SHUTDOWN, SHOW DATABASES, LOCK TABLES, REFERENCES, REPLICATION CLIENT, REPLICATION SLAVE, CREATE USER

[TOC](#toc)

## <a id="table-structure"></a>Table structure

#### Create table

```sql
CREATE TABLE [IF NOT EXISTS] `<table_name>` (
...
) ENGINE InnoDb CHARACTER SET utf8 COLLATE utf8_general_ci;
```

#### Copy table structure

```sql
CREATE TABLE `<destination_database>`.`<table_name>` LIKE `<source_database>`.`<table_name>`;
```

#### Rename table

```sql
RENAME TABLE `<database>`.`<old_table_name>` TO `<database>`.`<new_table_name>`;
```

#### Remove table

```sql
DROP TABLE [IF EXISTS] `<table_name>`;
```

[TOC](#toc)

## <a id="relations"></a>Relations

#### Show relations

```sql
SHOW CREATE TABLE `<table_name>` \G
```

#### Add relation

```sql
ALTER TABLE `<table_name>` ADD CONSTRAINT `<relation_name>` FOREIGN KEY `<index_name>` (`<column_name>`) REFERENCES `<related_table_name>` (`<related_column_name>`) ON DELETE [RESTRICT | CASCADE | SET NULL | NO ACTION];
```

#### Remove relation

```sql
ALTER TABLE `<table_name>` DROP FOREIGN KEY `<relation_name>`;
```

[TOC](#toc)

## <a id="misc"></a>Misc

#### Show MySQL version

```sql
SHOW VARIABLES LIKE "%version%";
```

#### Foreign key check

```sql
SET foreign_key_checks = 0;
SET foreign_key_checks = 1;
```

#### Reset auto increment

```sql
ALTER TABLE `<table_name>` AUTO_INCREMENT = 1;
```

#### Concatenate (non NULL) values from a group

```sql
SELECT `movie`, GROUP_CONCAT(`time` SEPARATOR ',') AS `running_times` FROM `schedule` WHERE `movie` = 'A Beautiful Mind' GROUP BY `movie` ORDER BY NULL
```

#### Search & Replace Data

```sql
UPDATE `<table_name>` SET `<field_name>` = REPLACE(`<field_name>`, '<string_to_find>', '<string_to_replace>');
```

#### Find duplicate records by a specific column

```sql
SELECT *, COUNT(<column>) AS dup FROM `<table>` GROUP BY <column> HAVING dup > 1
```

#### Delete duplicate records, but leave one

```sql
DELETE FROM <table> WHERE id NOT IN (SELECT * FROM (SELECT MIN(t.id) FROM <table> t GROUP BY t.<column>) x) -- keep records with the lowest ID
DELETE FROM <table> WHERE id NOT IN (SELECT * FROM (SELECT MAX(t.id) FROM <table> t GROUP BY t.<column>) x) -- keep records with the highest ID
```

```sql
DELETE t1 FROM <table> t1, <table> t2 WHERE t1.<column> = t2.<column> AND t1.id > t2.id -- keep records with the lowest ID
DELETE t1 FROM <table> t1, <table> t2 WHERE t1.<column> = t2.<column> AND t1.id < t2.id -- keep records with the highest ID
```

#### Troubleshooting

```sql
SHOW ENGINE INNODB STATUS;
```

#### Disable cache

Per query

```sql
SELECT SQL_NO_CACHE ...;
```

Per session, use `0` to turn OFF, `1` to turn ON. Accepted `<level>` values: `0`, `1`, `2`.

```sql
SET SESSION query_cache_type=<level>;
```

Globally

```sql
SHOW VARIABLES LIKE 'query_cache_size';
SET GLOBAL query_cache_size=0;
SET GLOBAL query_cache_size=<old_value>;
```

#### Backup/Restore

```shell
$ mysqldump [-h <host>] -u <user> -p [-d|--no-data] <database> [<table> ...] > <filename.sql>
$ mysql [-h <host>] -u <user> -p <database> < <filename.sql>
```

#### Duplicate index check

Use `pt-duplicate-key-checker` from [Percona Toolkit](https://www.percona.com/software/mysql-tools/percona-toolkit) ([documentation](https://www.percona.com/doc/percona-toolkit/2.2/index.html)).

#### Finding out largest tables on MySQL Server

```sql
SELECT CONCAT(table_schema, '.', table_name),
    CONCAT(ROUND(table_rows / 1000000, 2), 'M') rows,
    CONCAT(ROUND(data_length / ( 1024 * 1024 * 1024 ), 2), 'G') DATA,
    CONCAT(ROUND(index_length / ( 1024 * 1024 * 1024 ), 2), 'G') idx,
    CONCAT(ROUND(( data_length + index_length ) / ( 1024 * 1024 * 1024 ), 2), 'G') total_size,
    ROUND(index_length / data_length, 2) idxfrac
FROM information_schema.TABLES
ORDER BY data_length + index_length DESC
LIMIT 10;
```

[TOC](#toc)

## <a id="resources"></a>Resources

 - [Using group by on multiple columns](https://stackoverflow.com/questions/2421388/using-group-by-on-multiple-columns)

[TOC](#toc)
