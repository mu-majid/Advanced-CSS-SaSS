## Project Notes

* Review this link https://developers.google.com/web/fundamentals/performance/rendering

* We will nor focus much on architecture in this project. Only we will create `base`, `components`, and `layout`.

* CSS variables could be manipulated with javascript and could be used instead of preprocessor variables

* Prefer to use SVG over icon fonts, icon fonts usually fails on some browsers.

* to format an SVG icon, we need to set its height and width.

* Usually the side bar is a `ul` html element.

* When using SVGs in HTML, Prefer to use a sprite svg file, because it saves unnecessary http calls.

* z-index only works if the position property is set.

* With flexbox, when we want to create spaces between flex items, we could margin: auto trick.

* <figure> element is a good choice for user reviews.

* `z-index` only works if the position is set on the element. 

* Centring text in an an inline element like `a` could be done by using `line-height` property and setting it to the exact inline element height would center the content.

* the idea behind line height is that it adds same amount of pixels above and below the text-line.

* prefer to use percentages with line height (percentage is calculated from the font size).

* For Flexbox notes and a good illustration for `flex: grow shrink basis` property, check this [link](https://css-tricks.com/understanding-flex-grow-flex-shrink-and-flex-basis/) 