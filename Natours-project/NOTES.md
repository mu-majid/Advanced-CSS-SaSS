
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


## Side Notes :

  * Padding does not get inherited.

## What is Viewport ?

  * The viewport is the user's visible area of a web page.
  * The viewport varies with the device, and will be smaller on a mobile phone than on a computer screen.