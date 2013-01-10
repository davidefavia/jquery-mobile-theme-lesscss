jQuery Mobile theme with LessCSS
================================

This project aims to integrate [LessCSS](http://lesscss.org/ "LESS « The Dynamic Stylesheet language") with [jQuery Mobile](http://jquerymobile.com/ "jQuery Mobile") base theme as downloaded from [theme roller](http://jquerymobile.com/themeroller/ "jQuery Mobile theme rolller"). The project is actually based on [jQuery Mobile version 1.2.0](http://jquerymobile.com/blog/2012/10/02/announcing-jquery-mobile-1-2-0-final/ "jQuery Mobile version 1.2.0").

It compiles with both [LessElements](http://lesselements.com/ "LessElements") and [LessHAT](http://lesshat.com/ "LessHAT"). Conditional browser vendor prefixes is an idea _stolen_ from [LessHAT](http://lesshat.com/ "LessHAT").

Configuration
-------------
File <code>global.less</code> let you define which browser vendors prefixes you want to include and global variables for your jQuery Mobile application.

File <code>app.less</code> let you import all swatches you need (default: a,b,c,d,e), jQuery Mobile mixins and global variables. Just edit <code>app.less</code>
to import more or less options (e.g. a second mixins file, other swatches of few swatches).

Every swatch file (e.g. <code>swatch-a.less</code>) includes two sections: swatch variables (colors, dimensions, fonts) and css rules. You can edit everything you need to fit your application look and feel.

How to manually create new swatch
---------------------------------
If you don't know what a _theme swatch_ means in jQuery Mobile, [read here](http://jquerymobile.com/test/docs/api/themes.html "jQuery Mobile docs: themes").

If you need to add a swatch (e.g. called <code>f</code>) simply:

1. copy and paste <code>swatch-a.less</code> (inside <code>themes</code> directory) renaming it as <code>swatch-f.less</code>
2. open <code>swatch-f.less</code> with your preferred editor and:
	* search for <code>@a-</code> and replace with <code>@f-</code>
	* search for <code>.ui-bar-a</code> and replace with <code>.ui-bar-f</code>
	* search for <code>.ui-body-a</code> and replace with <code>.ui-body-f</code>
	* search for <code>.ui-overlay-a</code> and replace with <code>.ui-overlay-f</code>
	* search for <code>.ui-btn-up-a</code> and replace with <code>.ui-btn-up-f</code>
	* search for <code>.ui-btn-hover-a</code> and replace with <code>.ui-btn-hover-f</code>
	* search for <code>.ui-btn-down-a</code> and replace with <code>.ui-btn-down-f</code>
3. change what you need and save <code>swatch-f.less</code>
4. add <code>@import "swatch-f.less";</code> line to <code>app.less</code>
5. compile <code>theme.less</code> to <code>theme.css</code>

Contacts
--------
For any problem [file an issue](https://github.com/davidefavia/jquery-mobile-theme-lesscss/issues "jQuery Mobile theme LessCSS issues") or [ask me on Twitter](https://twitter.com/_davide "@_davide").

License [MIT](http://opensource.org/licenses/MIT "MIT license @opensource.org")
-------------------------------------------------------------------------------
Copyright (c) 2013 davide favia <davide.favia@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
