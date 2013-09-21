Deputy CSS
======

Deputy CSS is a simple CSS "library" with helpful css classes for common design requirements.

The project is generated with SASS.

It includes padding, margin, width, border, color, typography, and general helpers.

It's a little bit backwards from the "semantic only" school of thought but it's what I prefer.

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
```.pad-N, .pad-t-N, .pad-r-N, .pad-b-N and .pad-l-N``` (N being the iteration)

The same applies to margin.
```.m-N, .m-t-N, .m-r-N, .m-b-N and .m-l-N```

```.no-margin``` and ```.no-padding``` - These clear out margin and/or padding on an element.

Additional classes are available to clear margin/padding on certain sides.
ex. ```.no-pad-l, .no-m-l, .no-pad-tb, .no-m-lr```

There are also some special classes such as ```.m-auto``` which sets auto left and right margin.


<h3>Width</h3>

Width classes are generated from 1-100% as ```.w-1 {  } .... .w-100 {  }```

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


