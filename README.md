## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/bbauska/Cheat-Sheets/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Cheat Sheets

One to four page cheat sheets for mySQL, GitHub, Linux, Networking, MS Windows, etcetera

1.  [mySQL](https://github.com/bbauska/Cheat-Sheets/blob/main/mysql-cheat-sheet.md/)
2.  [Linux](https://github.com/bbauska/Cheat-Sheets/blob/main/2020%20-%20Linux%20-%20Command%20Line%20-%20Linux%20Command%20Line%20Cheat%20Sheet%20-%202pgs.pdf/)
3.  [WordPress](https://www.hostinger.com/tutorials/wordpress-cheat-sheet)
5.  [openWRT](https://miracoin.wordpress.com/category/linux/openwrt/)
6.  [jQuery](https://github.com/bbauska/Cheat-Sheets/blob/main/wsu-jquery-cheat-sheet.pdf)
7.  [HTML](https://github.com/bbauska/Cheat-Sheets/blob/main/WSU-HTML-Cheat-Sheet.pdf/)
8.  [CSS](https://github.com/bbauska/Cheat-Sheets/blob/main/CSS-Cheatsheet.pdf/)
9.  [JavaScript]
10. [MarkDown](https://github.com/bbauska/Cheat-Sheets/blob/main/resources/markdown.pdf/)
11. [PHP](https://github.com/bbauska/Cheat-Sheets/blob/main/2020%20-%20PHP%20-%20WSU%20php%20Cheat%20Sheet%20-%2038pgs.pdf/)
12. [Bitcoin/Blockchain Nakamoto Whitepaper](https://github.com/bbauska/Cheat-Sheets/blob/main/2007%20-%20Nakamoto%20Bitcoin%20Whitepaper%20-%20coinbase%20-%209pgs.pdf)
13. [Linux IP Network Command](https://github.com/bbauska/Cheat-Sheets/blob/main/2020%20-%20Linux%20-%20Networking%20-%20IP%20Command%20-%20Cheat%20Sheet%20-%203pgs.pdf)
      
![Dragnet 1968](https://user-images.githubusercontent.com/41387907/139372839-a95d0533-0ea8-4633-bd84-54716144d9eb.png)

---

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

Markdown Cheatsheet<a name="TOP"></a>
===================

- - - - 
# Heading 1 #

    Markup :  # Heading 1 #

    -OR-

    Markup :  ============= (below H1 text)

## Heading 2 ##

    Markup :  ## Heading 2 ##

    -OR-

    Markup: --------------- (below H2 text)

### Heading 3 ###

    Markup :  ### Heading 3 ###

#### Heading 4 ####

    Markup :  #### Heading 4 ####


Common text

    Markup :  Common text

_Emphasized text_

    Markup :  _Emphasized text_ or *Emphasized text*

~~Strikethrough text~~

    Markup :  ~~Strikethrough text~~

__Strong text__

    Markup :  __Strong text__ or **Strong text**

___Strong emphasized text___

    Markup :  ___Strong emphasized text___ or ***Strong emphasized text***

[Named Link](http://www.google.fr/ "Named link title") and http://www.google.fr/ or <http://example.com/>

    Markup :  [Named Link](http://www.google.fr/ "Named link title") and http://www.google.fr/ or <http://example.com/>

[heading-1](#heading-1 "Goto heading-1")
    
    Markup: [heading-1](#heading-1 "Goto heading-1")

Table, like this one :

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

```
First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell
```

Adding a pipe `|` in a cell :

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | \|

```
First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  |  \| 
```

Left, right and center aligned table

Left aligned Header | Right aligned Header | Center aligned Header
| :--- | ---: | :---:
Content Cell  | Content Cell | Content Cell
Content Cell  | Content Cell | Content Cell

```
Left aligned Header | Right aligned Header | Center aligned Header
| :--- | ---: | :---:
Content Cell  | Content Cell | Content Cell
Content Cell  | Content Cell | Content Cell
```

`code()`

    Markup :  `code()`

```javascript
    var specificLanguage_code = 
    {
        "data": {
            "lookedUpPlatform": 1,
            "query": "Kasabian+Test+Transmission",
            "lookedUpItem": {
                "name": "Test Transmission",
                "artist": "Kasabian",
                "album": "Kasabian",
                "picture": null,
                "link": "http://open.spotify.com/track/5jhJur5n4fasblLSCOcrTp"
            }
        }
    }
```

    Markup : ```javascript
             ```

* Bullet list
    * Nested bullet
        * Sub-nested bullet etc
* Bullet list item 2

~~~
 Markup : * Bullet list
              * Nested bullet
                  * Sub-nested bullet etc
          * Bullet list item 2

-OR-

 Markup : - Bullet list
              - Nested bullet
                  - Sub-nested bullet etc
          - Bullet list item 2 
~~~

1. A numbered list
    1. A nested numbered list
    2. Which is numbered
2. Which is numbered

~~~
 Markup : 1. A numbered list
              1. A nested numbered list
              2. Which is numbered
          2. Which is numbered
~~~

- [ ] An uncompleted task
- [x] A completed task

~~~
 Markup : - [ ] An uncompleted task
          - [x] A completed task
~~~

- [ ] An uncompleted task
    - [ ] A subtask

~~~
 Markup : - [ ] An uncompleted task
              - [ ] A subtask
~~~

> Blockquote
>> Nested blockquote

    Markup :  > Blockquote
              >> Nested Blockquote

_Horizontal line :_
- - - -

    Markup :  - - - -

_Image with alt :_

![picture alt](http://via.placeholder.com/200x150 "Title is optional")

    Markup : ![picture alt](http://via.placeholder.com/200x150 "Title is optional")

Foldable text:

<details>
  <summary>Title 1</summary>
  <p>Content 1 Content 1 Content 1 Content 1 Content 1</p>
</details>
<details>
  <summary>Title 2</summary>
  <p>Content 2 Content 2 Content 2 Content 2 Content 2</p>
</details>

    Markup : <details>
               <summary>Title 1</summary>
               <p>Content 1 Content 1 Content 1 Content 1 Content 1</p>
             </details>

```html
<h3>HTML</h3>
<p> Some HTML code here </p>
```

Link to a specific part of the page:

[Go To TOP](#TOP)
   
    Markup : [text goes here](#section_name)
              section_title<a name="section_name"></a>    

Hotkey:

<kbd>⌘F</kbd>

<kbd>⇧⌘F</kbd>

    Markup : <kbd>⌘F</kbd>

Hotkey list:

| Key | Symbol |
| --- | --- |
| Option | ⌥ |
| Control | ⌃ |
| Command | ⌘ |
| Shift | ⇧ |
| Caps Lock | ⇪ |
| Tab | ⇥ |
| Esc | ⎋ |
| Power | ⌽ |
| Return | ↩ |
| Delete | ⌫ |
| Up | ↑ |
| Down | ↓ |
| Left | ← |
| Right | → |

Emoji:

:exclamation: Use emoji icons to enhance text. :+1:  Look up emoji codes at [emoji-cheat-sheet.com](http://emoji-cheat-sheet.com/)

    Markup : Code appears between colons :EMOJICODE:
