
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

  ###### `float: left | right`:

  * causes the element to be taken out of its normal flow and shift it completely to the right or the left as far as possible until it touches the borders of the containing element.
  * inline elements and text will wrap around floated elements.
  * use `clear fixes` to adjust height of floated elements.

  ###### `box-decoration-break: {value}`:
  
  * The box-decoration-break property specifies how the background, padding, border, border-image, box-shadow, margin, and clip-path of an element is applied when the box for the element is fragmented.

## Side Notes :

  * Padding does not get inherited.
  * Every HTML element fas a default display, depending on what type of element it is. There are two display values: block and inline.
  * Block Elements: stretch out to the left and right as far as it can.
  * Inline Elements: takes up as much width as necessary. 
  * `h1` is the most important heading element for **SEO**.
  * [How to center and element vertically](https://vanseodesign.com/css/vertical-centering/)
  * display span as block will make it occupy full widhth available and add a line break.
  * to center a block element inside another block element => use the trick `margin: 0 auto`.
  * `calc` function allows us to mix units while doing calculations, also note these calc are done during browser's layout step (during site rendering by the visual formatting model).
  * centering a heading (text) could be done using a utility class (basically a div that wraps all text tags we want to center).
  * Utility classes keep out components reusable and allow us to use them independently, for example, having heading-secondary class (h2 element) and may be we will center it in one page and not the other, so we should use a utility class (div with class) to wrap that heading-secondary we want to center. Same also may be applied to margins bottom to a heading or something like that.
  * always define images widths and `left, right` positioning with `%` for responsive pages.
  * This [article](https://css-tricks.com/almanac/properties/p/perspective/) describes the difference between `perspective` and transform: perspective.
  * Centering a block element inside another block element (`margin: 0 auto`).
  * Best way to make space between an element and a floated element is to use transform, and not padding or margins.
  * For responsive web design, always remember, images needs a width (**ALWAYS**).
  * there is no way two transform properties to be applied in the same time right now in css.
  * Sibling selectors in CSS is used to select either a direct sibling (+) (an html element right after the one we are selecting) or a general sibling (~) (any html after the element we are selecting on the same level)
  * `em` is calculated from the font-size of the element the unit is used on.

## What is Viewport ?

  * The viewport is the user's visible area of a web page.
  * The viewport varies with the device, and will be smaller on a mobile phone than on a computer screen.

## CSS Animations: 

  * There are two types of animations in CSS:
    1. Using transition property and change properties we want to animate on an event (like hovering an element).
    2. Using `@keyframes` rules.

  * the browser is [optizimed](https://developers.google.com/web/fundamentals/design-and-ux/animations/animations-and-performance) for using `opacity` and `transform` for the animations.

## Psuedo Elements:

  *selector::psuedo-element*

  * A CSS pseudo-element is used to style specified parts of an element.
  * For example: 
    1. Style the first letter, or line, of an element.
    2. Insert content before, or after, the content of an element.
    3. `::after`:  it adds like a virtual element after the original element and CSS3 allow us to style that virtual element.

  * Note that:

        The double colon replaced the single-colon notation for pseudo-elements in CSS3. This was an attempt from W3C to distinguish between pseudo-classes and pseudo-elements.

        The single-colon syntax was used for both pseudo-classes and pseudo-elements in CSS2 and CSS1.

        For backward compatibility, the single-colon syntax is acceptable for CSS2 and CSS1 pseudo-elements.


## Why and How to use `rem/em`?

  - because we want an easy way to change measurements in our page with one simple setting, meaning, **REMEMBER** that `rem` is calculated relative to the root `font-size`. And changing this root size will affect all our measurements if they were in `rem`s.

  - This is alternative to writing 100s of lines of media queries.

  - Note that old IE browsers does not support `rem`. 

## Responsive Design Principles: 

  - Fluid Grids and Layouts: To allow content to easily adapt to the current viewport width used to browse the website, Use `%` rather than `px` for all layout-related lengths (like width).

  - Flexible and responsive images: Images don't adapt like text to the viewport, so make sure they adapt by using adaptive/responsive widths. (more on that later)

  - Media Queries: change styles on certain viewport widths (breakpoints), allowing us to create different version of our website for different widths.

  ### Layout Types:

  * There exist three types of layouts: 

  **Float Layouts**: put boxes side-by-side (oldest type and most widely used)

  **Flexbox**: laying element in one dimensional row.

  **CSS Grid**: used for a 2-d layout page.

## Designing a Custom Grid:

 - Divide the page to rows and columns.
 - The row's max-width as a rule of thumb is defined to be 1140px (114rem - where the root font-size is 10px)