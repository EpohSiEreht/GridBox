GridBox v2
===========
A responsive, fluid 12-column css grid framework based on CSS Grid Layout module.
- Nestable
- Mobile First
- Semantic class names

## What is CSS Grid Layout?
CSS Grid Layout is a two-dimensional layout system, optimized for customizable column and row layouts.

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

Or you can use this CDN and add it in your head tag
```html
<link rel="stylesheet" href="https://unpkg.com/gridbox/gridbox.css">
```

## Guidelines
- Unlike Bootstrap's grid system, you do not need to include a row class. 
- Nesting should be done by adding the sub-item class with the column class.
- .col-xs-* should not be nested under a row that has a .col-xs-* parent.
- Content should be placed within columns unless you are nesting child columns.
- Any child div of within the gridbox container will default to the full width of the parent.
- Gutters are set to 1rem (16px) as default and go up to 1.5rem (24px) on screens larger than 960px wide.
- Use \<header> for the header, \<main> for the main content body, and \<footer> for the footer.
- Columns go from 1 to 12.
- Breakpoints: 
    - 0px - 599px (col-xs-\*)
    - 600px - 959px (col-sm-\*)
    - 960px - 1279px (col-md-\*)
    - 1280px - 1919px (col-lg-\*)
    - 1920px and above (col-xl-\*)

## Example

```html
<div class="container">
    <header>Header</header>
    <main>
        <div class="col-md-8 sub-items">
            <div class="col-md-4">col-md-4</div>
            <div class="col-md-4">col-md-4</div>
            <div class="col-md-4">col-md-4</div>
        </div>
        <div class="col-md-4 sub-items">
            <div class="col-md-6">col-md-6</div>
            <div class="col-md-6">col-md-6</div>
            <div class="col-sm-12">col-sm-12</div>
        </div>
        <div class="col-xs-3">col-xs-3</div>
        <div class="col-xs-9">col-xs-9</div>
    </main>
    <footer>Footer</footer>
</div>
```

## Demo
Codepen demo for v2: [https://codepen.io/epohsiereht/pen/aWPpZd](https://codepen.io/epohsiereht/pen/wdLQpM)

## Differences between v1 and v2
Version 1 followed the same syntax as Bootstrap. After receiving feedback, I realized that Grid Layout is about semantic class names rather than presentational class names. So I removed the row wrapper and opted to just add a sub-items class along with the column class to set up nested columns.
1. Removed the row class wrapper.
2. To nest, you just need to add .sub-items class along with the column class.
3. Added grids for \<header>, \<main>, and \<footer> tags.

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
- Add vertical and horizontal alignment classes.
- Add design guidelines for typography, forms, buttons, etc.
- Add pre-built and reusable component layouts using CSS Grid and Flexbox Layout modules.

## Resources
- [CSS TRICKS - CSS Grid Layout](https://css-tricks.com/snippets/css/complete-guide-grid)
- [MDN - CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [W3C Editor's Draft](https://drafts.csswg.org/css-grid)
- [Grid by Example](https://gridbyexample.com/)