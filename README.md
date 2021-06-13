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

# Commands
To get the raw contents of the Rituum.
```js
var str = rituum.blob();
```

To get the contents of the Rituum window
```js
var str = rituum.window();
```

To get the contents of the current selection made with the mouse.
```js
var str = rituum.selection();
```

Note you can set the mode by clicking on the `m`. This toggles between __RTM__NUCLEOTIDE and __RTM__BINARY.

# Copy and paste
Although the Rituum is drawn on canvas, you can still copy and paste using a selection you make with the mouse, 
or by clicking on the `c` button. This will copy the contents of any specific Rituum onto the clipboard.
