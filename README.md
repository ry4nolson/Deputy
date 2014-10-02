Deputy CSS
======

Deputy CSS is a simple CSS "mini-library" with helpful css classes for common design requirements.

see GitHub page here http://ry4nolson.github.io/Deputy/

The project is generated with SASS.

It includes padding, margin, width, border, color, typography, and general helpers.

It's a little bit backwards from the "semantic only" school of thought but it has practical purposes.  Building with deputy allows for a more modular site build to allow less knowledgeable end users to duplicate and modify elements quickly and easily.

Examples
=====


<h3>Padding and Margin</h3>

"I want this div to have 20 pixels of padding"
--- Some guy

```html
<div class="pad-20">
  stuff
</div>
```
  
Also included are helpers to apply padding to only certain sides of an element

"I want 20 pixels of padding on the left side of this div"
--- Same guy as before

```html
<div class="pad-20 pad-l-only">
  stuff
</div>
```
or
```html
<div class="pad-l-20">
  stuff
</div>
```

Padding and Margin classes are generated in increments of 5 up to 100. Each increment has 5 rules: 
```css
/* padding 20 */
.pad-20 { padding: 20px !important; }
.pad-t-20 { padding-top: 20px !important; }
.pad-r-20 { padding-right: 20px !important; }
.pad-b-20 { padding-bottom: 20px !important; }
.pad-l-20 { padding-left: 20px !important; }
...
/* margin 20 */
.m-20 { margin: 20px !important; }
.m-t-20 { margin-top: 20px !important; }
.m-r-20 { margin-right: 20px !important; }
.m-b-20 { margin-bottom: 20px !important; }
.m-l-20 { margin-left: 20px !important; }
```


```.no-margin``` and ```.no-padding``` - These set padding/margin to 0 on an element

Additional classes are available to clear margin/padding on certain sides.
ex. ```.no-pad-l, .no-m-l, .no-pad-tb, .no-m-lr```

There are also some special classes such as ```.m-auto``` which sets auto left and right margin.


<h3>Width</h3>

Width classes are generated from 1-100% as ```.w-1 {  } .... .w-100 {  }```

Width classes are also generated in a fractional format such as ```.w-1-5```. This means 1/5 width or 20%.
Fraction denomintors are generated from 2 to 24
```css
.w-1-2 { width: 49.99% !important; }
...
.w-5-14 { width: 35.70429% !important; }
...
.w-23-24 { width: 95.82333% !important; }
```
.01 is subtracted from every value just to not have to deal with weird rounding stuff.


<h3>Border</h3>

Border classes are generated from 1-10 such as 
```css
/* border-3 */
.border-3 { border: 3px solid; }
.border-t-3 { border-top: 3px solid; }
.border-r-3 { border-right: 3px solid; }
.border-b-3 { border-bottom: 3px solid; }
.border-l-3 { border-left: 3px solid; }
```

this can be combined with other border classes for color and style.

```html
<div class="border-b-1 border-dashed border-grey">
  some thing
</div>
```

<h3>Colors</h3>

The ```_variables.scss``` file contains 6 color variables from black to white.

The defaults are:
```scss

$black: #000;
$white: #fff;
$grey: #999;
$lightGrey: #e5e5e5;
$mediumGrey: #ccc;
$darkGrey: #222;
```

These are used to create border, text color, and background classes

The color by itself is a font color class.
ex: 
```css
.medium-grey { color:$mediumGrey; }
```

Prefix ```bg-``` for background color and ```border-``` for border color.

The colors in the css are 
```
black, light-grey, medium-grey, grey, dark-grey, white|fff
```
