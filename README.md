GridBox
===========
A responsive, fluid 12-column css grid framework based on CSS Grid Layout. It is nestable and uses the same syntax as Bootstrap's Grid system so you can switch with ease. 

## What is CSS Grid Layout?
CSS Grid Layout is a two-dimensional layout system, optimized for customizable column and row layouts. No more floats, inline-block, and table grid setups!

## Getting Started
NPM
```javascript
npm install --save gridbox
```
Import
```js
// ES5
require('gridbox/gridbox.css')

// ES6
import "gridbox/gridbox.css"
```

You can also use this link tag and add it to your head tag
```html
<link rel="stylesheet" href="https://unpkg.com/gridbox@1.0.1/gridbox.css">
```

## Guidelines
- Rows should be directly placed within a .container(fixed-width) or .container-fluid (full-width)
- Nesting should be done by adding a row class within a column class.
- .col-xs-* should not be nested under a row that has a .col-xs-* parent.
- Columns should not be directly placed as a child of another column.
- Content should be placed within columns.
- Any non-row/column class divs will automatically fill the entire row or column width.
- Gutters are set to 1rem (16px) as default and go up to 1.5rem (24px) on screens larger than 960px wide.
- Breakpoints: 
    - 0px - 599px (col-xs-\*)
    - 600px - 959px (col-sm-\*)
    - 960px - 1279px (col-md-\*)
    - 1280px - 1919px (col-lg-\*)
    - 1920px and above (col-xl-\*)

## Example

```html
<div class="container">
  <div class="row">
    <div class="col-md-6">col-md-6</div>
    <div class="col-md-6">col-md-6</div>
  </div>
  <div class="row">
    <div class="col-sm-12">col-sm-12</div>
  </div>
  <div class="row">
    <div class="col-md-8">
        <div class="row">
            <div class="col-md-4">col-md-4</div>
            <div class="col-md-4">col-md-4</div>
        </div>
    </div>
  </div>
</div>
```

## Demo
Codepen demo: [https://codepen.io/epohsiereht/pen/aWPpZd](https://codepen.io/epohsiereht/pen/aWPpZd)

## Browser Support
| Browser             | Compatibility           | Version  |
| ------------------- |-------------------------| ------- |
| Chrome              | YES                     | 57+  |
| FireFox             | YES                     | 52+  |
| Safari              | YES                     | 10.1 |
| Opera               | YES                     | 44+  |
| IE                  | PARTIAL                 | 11* |
| Edge                | PARTIAL                 | 14*, 15* |
| iOS Safari          | YES                     | 10.3 |
| Chrome for Android  | YES                     | 57  |
| Android Browser     | NO                      |  |
| Opera Mobile        | NO                      |  |
| Opera Mini          | NO                      |  |
> Note: Partial support for IE and Edge is based on an older specification of CSS Grid from 2011. 

## Future Features++
- Add offset column classes.
- Add design guidelines for typography, forms, buttons, etc.
- Add pre-built and reusable component layouts using the Flexbox Layout module.

## Resources
- [CSS TRICKS - CSS Grid Layout](https://css-tricks.com/snippets/css/complete-guide-grid)
- [MDN - CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [W3C Editor's Draft](https://drafts.csswg.org/css-grid)
- [Grid by Example](https://gridbyexample.com/)