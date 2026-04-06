/* from Rico's Cheatsheets */
<!------------------------------------------------------------------------------------------------>
<h1><a href="https://devhints.io/">Rico's cheatsheets (by developers for developers)</a></h1>
<!------------------------------------------------------------------------------------------------>
/* SASS */
<h2><a href="https://devhints.io/sass">SASS Cheatsheet</a></h2>
<!------------------------------------------------------------------------------------------------>
<h2><a href="https://sass-lang.com/documentation">SASS</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Sass is a stylesheet language that’s compiled to CSS. It allows you to use variables, nested rules, mixins, functions, and more, all with a fully CSS-compatible syntax. Sass helps keep large stylesheets well-organized and makes it easy to share design within and across projects.</p>
<p>Sass is the most mature, stable, and powerful professional grade CSS extension language in the world.</p>
<!------------------------------------------------------------------------------------------------>
<!-- JS React -->
<h2><a href="https://devhints.io/react">JS React</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Components, States, Nesting, Import multiple exports, Properties, Children, Default properties 
and state, Functional &amp; Pure components, Component API, Lifecycle Mounting &amp; Updating, Hooks 
(New) State and Building your own hooks, Declaring multiple state variables, Effect hook, Hooks API 
Reference, DOM nodes, References and DOM Events, Other features: Transferring props and Top-level 
API's, JSX patterns: Style shorthand, Lists, Inner HTML, Conditionals, Short-circuit evaluations, 
New featues: Returning multiple elements, returning strings, Portals, Errors, Hydration, Property 
validation: PropTypes, Basic Types, Arrays and objects, Required types, Elements, Custom validation, 
Enumerables (oneOf)</p>
<ul>
  <li>Also see: <a href="https://reactjs.org/">Reactjs.org</a></li>
  <li><a href="https://reactcheatsheet.com/">React cheatsheet</a></li>
  <li><a href="https://github.com/enaqx/awesome-react">Awesome React</a></li>
  <li><a href="https://devhints.io/react@0.14">React v0.14 cheatsheet Legacy version</li>
</ul>
<!------------------------------------------------------------------------------------------------>
<!-- Markdown -->
<h2><a href="https://devhints.io/markdown">Markdown</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Headers, Lists, Code, Emhasis, Links, Blockquotes, Images, Horizonal line, &amp; Tables.</p>
<!------------------------------------------------------------------------------------------------>
<!-- Haml -->
<h2><a href="https://devhints.io/haml">Haml Cheatsheet</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Doctype, Inline attributes, Tags, Ruby, &amp; Classes and ID's.</p>
<!------------------------------------------------------------------------------------------------>
<!-- package.JSON -->
<h2><a href="https://devhints.io/package-json">package.JSON</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Basic, Scripts, Misc, Config, Dependencies, and 
<a href="http://package.json.nodejitsu.com/">References</a>.</p>
<!------------------------------------------------------------------------------------------------>
<!-- tar -->
<h2><a href="https://devhints.io/tar">tar CheatSheet</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Deflate/Inflate/Concatenate and Common options.</p>
<!------------------------------------------------------------------------------------------------>
<!-- cURL -->
<h2><a href="https://devhints.io/curl">cURL</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Options, Data, Headers, Request, SSL.</p>
<!------------------------------------------------------------------------------------------------>
<!-- CSS Bootstrap -->
<h2><a href="https://devhints.io/bootstrap">CSS Bootstrap</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Screen sizes, Modal, Modal via ajax (Rails), Columns, Tooltip, Utilities, and Input groups.</p>
<!------------------------------------------------------------------------------------------------>
<!-- CSS Grid -->
<h2><a href="https://devhints.io/css-grid">CSS Grid</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Container, Child, and References:</p>
<ul>
  <li><a href="http://grid.malven.co/">GRID: A simple visual cheatsheet</a></li>
  <li><a href="https://css-tricks.com/snippets/css/complete-guide-grid/">CSS Tricks: A Complete Guide to Grid</a></li>
  <li><a href="https://caniuse.com/#feat=css-grid">Browser support</a></li>
</ul>
<!------------------------------------------------------------------------------------------------>
<h2><a href="https://devhints.io/css-tricks">CSS Tricks</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Heading kerning pairs and ligature, iOS Scrolling prevention, Native-like iOS scrolling, Gradient 
text, Text stroke, UIWebView optimizations, and Browser hacks.</p>
<p>Mozilla-only</p>
<pre>
@-moz-document url-prefix() {
  .box { color: blue; }
}
</pre>
<p>Webkit-only</p>
<pre>
@media all and (-webkit-min-device-pixel-ratio: 1) {
}
</pre>
<!------------------------------------------------------------------------------------------------>
<!-- CSS Flexbox -->
<h2><a href="https://devhints.io/css-flexbox">CSS Flexbox</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Simple example, Child, Container, Tricks.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Vertical center</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<pre>
.container {
  display: flex;
}

.container > div {
  width: 100px;
  height: 100px;
  margin: auto;
}
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Mobile layout</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<pre>
.container {
  display: flex;
  flex-direction: column;
}

.container > .top {
  flex: 0 0 100px;
}

.container > .content {
  flex: 1 0 auto;
}
</pre>
<p>A fixed-height top bar and a dynamic-height content area.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Vertical center (2)</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<pre>
.container {
  display: flex;
  align-items: center;     /* vertical */
  justify-content: center; /* horizontal */
}
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Reordering</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<pre>
.container > .top {
 order: 1;
}

.container > .bottom {
 order: 2;
}
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Table-like</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<pre>
.container {
  display: flex;
}

/* the 'px' values here are just suggested percentages */
.container > .checkbox { flex: 1 0 20px; }
.container > .subject  { flex: 1 0 400px; }
.container > .date     { flex: 1 0 120px; }
</pre>
<p>This creates columns that have different widths, but size accordingly according to the circumstances.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Vertical</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<pre>
.container {
  align-items: center;
}
</pre>
<p>Vertically-center all items</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Left and right</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<pre>
.menu > .left  { align-self: flex-start; }
.menu > .right { align-self: flex-end; }
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>References</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ul>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Flexible_boxes">MDN: Using CSS flexbox</a></li>
  <li><a href="https://www.sketchingwithcss.com/samplechapter/cheatsheet.html">Utlimate flexbox cheatsheet</a></li>
</ul>
<!------------------------------------------------------------------------------------------------>
<!-- CSS Cheatsheet -->
<h2><a href="https://devhints.io/css">CSS Cheatsheet</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Selectors, Attribute Selectors, Pseudo-class variations, Combinators, Pseudo-classes, Fonts, 
Background, Animation.</p>
<!------------------------------------------------------------------------------------------------>
<!-- SASS -->
<h2><a href="https://devhints.io/sass">SASS Cheatsheet</a></h2>
<!------------------------------------------------------------------------------------------------>
<p><a href="">Introduction</a>, <a href="">Documentation</a>, Mixins, Extend, Variables, Composing 
Nesting, and Comments.</p>
<p>Color functions</p>
<p>rgba, Getting individial values, Mixing, Modifying HSLA, and Adjustments.</p>
<p>Other functions</p>
<p>Strings, Numbers, Units, Misc.</p>
<p>Feature checs and Features.</p>
<p>Loops</p>
<p>For loops, Each loops (nested), Each loops (simple), and While loops.</p>
<p>Other features</p>
<p>Conditionals, Lists, Maps, and Interpolation.</p>
<p>See also</p>
<ul>
  <li><a href="http://sass-lang.com/documentation/Sass/Script/Functions.html">Also 1</a></li>
  <li><a href="http://sass-lang.com/documentation/file.SASS_REFERENCE.html#sassscript">Also 2</a></li>
</ul>
<!------------------------------------------------------------------------------------------------>
<!-- Stylus -->
<h2><a href="https://devhints.io/stylus">Stylus Cheatsheet</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Mixins, Functions, values, and Advanced features, Built-in functions.</p>
<!------------------------------------------------------------------------------------------------>
<!-- Node JS Assert -->
<h2><a href="https://devhints.io/nodejs-assert">Node JS Assert Cheatsheet</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Assertions and References.</p>
<!------------------------------------------------------------------------------------------------>
<!-- LESS.js -->
<h2><a href="https://devhints.io/less">Less.js Cheatsheet</a></h2>
<!------------------------------------------------------------------------------------------------>
<p>Functions and Conditionals.</p>
<!------------------------------------------------------------------------------------------------>
<h2>HOW TO BUILD A COMIC BOOK STORE w/Meusa,Gatsby,PayPal, and MeiliSearch</h2>
<!------------------------------------------------------------------------------------------------>
<h3><a href="https://medusajs.hashnode.dev/how-i-built-a-comic-book-store-from-scratch-with-medusa-gatsby-paypal-and-meilisearch">From Scratch</a></h3>
<!------------------------------------------------------------------------------------------------>
<h2><a href="https://onose.hashnode.dev/a-ride-with-css-continued">Build a restaurant menu page</a></h2>
<!------------------------------------------------------------------------------------------------>
<!-- Major Cloud Providers -->
<h2><a href=https://free-for.dev/#/?id=major-cloud-providers">Major Cloud Providers</a></h2>
<!------------------------------------------------------------------------------------------------>
<p></p>
<!------------------------------------------------------------------------------------------------>

