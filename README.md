# Overview:

  * This Repository was created/updated during taking a course by [Jonas Schmedtmann](https://codingheroes.io/)
  * This repo contains three main projects that uses `Advanced` css technologies, namely:

    1. Natours Project (Advanced CSS with SaSS)
    2. Trillo Project (Flexbox)
    3. Nexter Project (CSS Grid layouts)

  * Each project Directory will have a README file with notes about challenges and gotchas faced during building the project.

## How CSS Works? (Behind The Scene):

  #### Three Golden Rules When Building HTML & CSS:

  1. Responsive Design: Websites should work responsively to any device they work on, topics like fluid layouts, media queries, responsive images, correct units, and desktop-first vs mobile-first approaches are crucial.

  2. Maintainable and scalable code: topics like how to organize files, how to name html classes, and even how to structure HTML tags.

  3. Web Performance: less size, and fast app. Somethings to consider are less HTTP requests, Less Code, Compress Code, use CSS preprocessor (like SaSS), **less images**, and compress images.

  #### What Actually Happens?

  ##### Overview

  * The step `Process final CSS Values` is when units like `%` gets converted to `px`.
  * the visual formatting model uses the `box-model`, `floats` and `positioning` to render the CSS.

  ![overviewbrowser](./pics/overview-browser.png)

  ##### CSS Parsing phase - cascading step:

  * A css rule consists of a selector and a declaration block.
  * Step One: Cascading. When combining different stylesheets and resolving conflicts between different CSS rules and declarations when more than one rule apply to certain element.
  * There are three types of stylesheets (Author, user, browser) - Author: is what we write as developers, user: when a user change his browser font size, and browser: default appearance of tags differ from browser to another one.

  * **BUT how conflicts are resolved?** => First look at the *Importance*, then *Selector Specificity*, and the *source order*.

  ![conflict](./pics/conflict-css.png)

  * An Example of how specificity is calculated:
    - Each rule will be assigned a tuple of numbers, and then compare the first number in all tuple, if there is a tie, move to second number and compare them (only the rules with a tie), until reaching the last number.
    - The value/rule chosen is called cascaded value. 

  ![spec-conflict](./pics/spec-conflict.png)

  - Declarations with `!important` have the highest priority.
  - but avoid using them in favor of writing maintainable code.
  - inline styles will always have priority over styles in the stylesheets.
  - Selector with **one** ID is more specific than a one with **1000** classes.
  - The universal selector `*` has a specificity of `(0, 0, 0, 0)`.
  - Always rely on specificity, not order, not inline, not important, so that the code would be more maintainable.
  - But rely on order when using 3rd-party library - always put your author stylesheet last.


  ##### CSS value parsing - value processing step:

  * Any value goes through a six steps conversion process as indicated below.

  ![valueparsing](./pics/value-parsing.png)

  * Also, the relative units get converted to pixels as indicated below:

  ![relativeconvert](./pic/relative-units.png)

  * Each property has an initial value, used if nothing is declared (and if there is no inheritance);
  * Browsers specify a root font-size for each page (usually 16px);
  * Percentages and relative values are always converted to `pixels`;
  * Percentages are measured relative to their **parent’s** `font-size`, if used to specify `font-size`;
  * Percentages are measured relative to their **parent’s** `width`, if used to specify `lengths`;
  * `em` are measured relative to their **parent** `font-size`, if used to specify `font-size`;
  * `em` are measured relative to the **current** `font-size`, if used to specify `lengths`;
  * `rem` are always measured relative to the document’s **root** font-size;
  * vh and vw are simply percentage measurements of the viewport’s height and width.
