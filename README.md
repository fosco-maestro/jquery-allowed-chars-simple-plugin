# jQuery Allowed Chars - simple plugin


jQuery plugin to restrict users for typing only allowed chars for specified element.

This library requires [jQuery][1] to be loaded.

## Setup

Include  jQuery library and the `jquery.allowed-chars.js` file.

```html
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js"></script>
<script type="text/javascript" src="dist/jquery.allowed-chars.js"></script>
```

### Download plugin from jQuery Plugins

You can download jQuery Allowed Chars simple plugin from [jQuery Plugins][8] here:
[http://plugins.jquery.com/jquery.allowed-chars/][7]

### Install with Bower

Install and manage jQuery Allowed Chars simple plugin using [Bower][4].

```
$ bower install jquery.allowed-chars
```

### Install with NPM

Install and manage jQuery Allowed Chars simple plugin using [NPM][5].

```
$ npm install jquery.allowed-chars
```

### CDN

You can use [CDNJS][10] for this plugin on following link:
[http://www.cdnjs.com/libraries/jquery.allowed-chars][9]

Usage Example
-------------

In our HTML code we have 4 inputs:

```html
Only integer chars [0123456789]: 
<input type='text' id="default"/>

Custom chars [a, B, 1, {space}, _]: 
<input type='text' id="custom"/>

RegExp [/\d/] -- only integers: 
<input type='text' id="regexp" />

Custom chars [A, b, s, D] not case sensitive, full options: 
<input type='text' id="full" />
```

So, to restrict input values to integers for input with id `default` use:

```js
// by default plugin allows only numberical characters: 0123456789
$('#default').allowedChars();
```

For a custom allowed char list, pass the string with chars as parameter:

```js
// you can specify a different list of allowed characters,
// for example [a, B, 1, {space}, _]
// list is by default case sensitive
$('#custom').allowedChars('aB1 _');
```

You can also use a regular expression to restrict input values:

```js
// you can use regular expressions
// \d - only integers allowed
$('#regexp').allowedChars(/\d/);
```

You can also pass an object with options for plugin initialization:

```js
// you can pass object with options.
// For example, a list of allowed chars, without case sensititvity check
$('#full').allowedChars({
    allowed: 'AbsD',
    caseSensitive: false
});
```

Be aware that `caseSensitive` option does not affect work of plugin if you use regular expressions.

Here you can read more about regular expressions in javascript: [http://www.w3schools.com/jsref/jsref_obj_regexp.asp][6]

Demo
----

You can run demo on [JSFiddle][3]: [http://jsfiddle.net/fosco/55XLd/][2]

[1]: http://jquery.com/
[2]: http://jsfiddle.net/fosco/55XLd/
[3]: http://jsfiddle.net/
[4]: http://bower.io/
[5]: https://www.npmjs.org/
[6]: http://www.w3schools.com/jsref/jsref_obj_regexp.asp
[7]: http://plugins.jquery.com/jquery.allowed-chars/
[8]: http://plugins.jquery.com/
[9]: http://www.cdnjs.com/libraries/jquery.allowed-chars
[10]: http://www.cdnjs.com/
