
## What is CSS Reset ?

  * A CSS Reset (or “Reset CSS”) is a short, often compressed (minified) set of CSS rules that resets the styling of all HTML elements to a consistent baseline.

  * In case you didn’t know, every browser has its own default ‘user agent’ stylesheet, that it uses to make unstyled websites appear more legible. For example, most browsers by default make links blue and visited links purple, give tables a certain amount of border and padding, apply variable font-sizes to H1, H2, H3 etc. and a certain amount of padding to almost everything. Ever wondered why Submit buttons look different in every browser?

  * Using a CSS Reset, CSS authors can force every browser to have all its styles reset to null, thus avoiding cross-browser differences as much as possible.

## What is Universal Selector ?

  * The Universal Selector is the * in CSS. Literally the asterisk character. It is essentially a type selector that matches any type. Type meaning an HTML tag like <div>, <body>, <button>, or literally any of the others.

  * A common use is in the universal reset, like this:

  ```javascript
    {
      margin: 0;
      padding: 0;
    }
  ```

## What is {{CSS Property}} ?

  ###### `box-sizing: border-box`:
  * change the box model, so that the borders and the paddings **are no longer** added to the total width or the total height.
  * By default, the width and height of an element is calculated like this:

        width + padding + border = actual width of an element
        height + padding + border = actual height of an element

  * This means: When you set the width/height of an element, the element often appears bigger than you have set (because the element's border and padding are added to the element's specified width/height).

  ###### `line-height: {value}`:

  * The line-height CSS property sets the height of a line box. It's commonly used to set the distance between lines of text.
  * check this [link](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)

  ###### `position: {value}`:

  * Specify where an element should be positioned (static, relative, absolute, fixed, sticky)
  * relative positioning is calculated **relative** to the normal (default) position of the element in HTML.
  * absolute positioning is calculated from page borders, or if absolute element is inside an element, it will be positioned relative the parent's borders.

  ###### `text-decoration: {value}`:

  * The text-decoration property specifies the decoration added to text, and is a shorthand property for:
      text-decoration-line (required)
      text-decoration-color
      text-decoration-style

  ###### `display: {inline-block}`:

  * Compared to `display: inline`, the major difference is that `display: inline`-block allows to set a width and height on the element.
  * Also, with `display: inline-block`, the top and bottom margins/paddings are respected, but with display: inline they are not.
  * Compared to `display: block`, the major difference is that `display: inline-block` does not add a line-break after the element, so the element can sit next to other elements.

## Side Notes :

  * Padding does not get inherited.
  * Every HTML element fas a default display, depending on what type of element it is. There are two display values: block and inline.
  * Block Elements: stretch out to the left and right as far as it can.
  * Inline Elements: takes up as much width as necessary. 
  * `h1` is the most important heading element for **SEO**.
  * [How to center and element vertically](https://vanseodesign.com/css/vertical-centering/)
  * display span as block will make it occupy full widhth available and add a line break

## What is Viewport ?

  * The viewport is the user's visible area of a web page.
  * The viewport varies with the device, and will be smaller on a mobile phone than on a computer screen.

## CSS Animations: 

  * There are two types of animations in CSS:
    1. Using transition property and change properties we want to animate on an event (like hovering an element).
    2. Using `@keyframes` rules.

  * the browser is [optizimed](https://developers.google.com/web/fundamentals/design-and-ux/animations/animations-and-performance) for using `opacity` and `transform` for the animations.

