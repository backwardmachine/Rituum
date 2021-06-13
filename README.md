# Rituum
A small widget for displaying DNA nucleotide sequences in a browser, and converting to binary code and other data formats. HTML and Javascript.

![rituum](ss13062021.jpg)

# Getting started
To get started include the minified javascript file `rtm.js` in your header.
```html
<script src="rtm.js"></script>
```

You need a HTML containing element for each sequence. Make an element `<div id="container"></div>` and the rituum will nest inside of it.
```js
var rituum = new neodna__Rituum();
rituum.init();
rituum.nest( "container" );
```

Each Rituum is setup with two basic modes, `__RTM__NUCLEOTIDE` and `__RTM__BINARY`. Here we set it to nucleotide anyway.
```js
rituum.mode( __RTM__NUCLEOTIDE );
```

# Setting the sequence
We can input our sequence quickly and draw it on the page.
```js
rituum.set( 'CCTACATTTCCTTTATTCATATTCTTTTTATTTTCTTGCCAATTCC' );
rituum.draw( 1 );
```
