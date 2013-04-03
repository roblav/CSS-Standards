---
layout: blog_post
title: 4. Preprocessor
---

### Beware of bloated CSS

Utilise a preprocessors features such as mixins, variables, nested rules and functions to make code easier to maintain but always double check compiled stylesheets to avoid code bloat.  Preprocessors, when used inefficiently, can cause code bloat.

Source: [SMACSS on preprocessors (members only)](https://smacss.com/book/preprocessors)

##Additional format considerations

Different CSS preprocessors have different features, functionality, and syntax. Your conventions should be extended to accommodate the particularities of any preprocessor in use. The following guidelines are in reference to Sass.

* Limit nesting to 1 level deep. Reassess any nesting more than 2 levels deep. This prevents overly specific CSS selectors.
* Avoid large numbers of nested rules. Break them up when readability starts to be affected. Preference to avoid nesting that spreads over more than 20 lines.
* Always place @extend statements on the first lines of a declaration block.
* Where possible, group @include statements at the top of a declaration block, after any @extend statements.
* Consider prefixing custom functions with x- or another namespace. This helps to avoid any potential to confuse your function with a native CSS function, or to clash with functions from libraries.

Example:

    .selector-1
        @extend .other-rule
        @include clearfix()
        @include box-sizing(border-box)
        width: x-grid-unit(1)
        // other declarations
  

Source: [Principles of writing consistent, idiomatic CSS by Nicolas Gallagher](https://github.com/necolas/idiomatic-css)

