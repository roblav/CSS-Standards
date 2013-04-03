---
layout: blog_post
title: Properties
categories : [format]
---

* Include one declaration per line in a declaration block.
* For each declaration use one level of indentation, two spaces, not tabs.
* Include single space after the colon of a declaration. (This is also good practise when switching to using SASS the space is required.)
* Use lowercase and shorthand hex values, e.g., #aaa.
* Where allowed, avoid specifying units for zero-values, e.g., margin: 0.
* Include a space after each comma in comma-separated property or function values.
* End each  declaration with a semi-colon.
* Place the closing brace of a ruleset in the same column as the first character of the ruleset.
* Separate each ruleset by a blank line.

Example code:

    #forum .description {
      color: #efefef;
      font-size: 0.9em;
      margin: 0.5em;
    }
    
Source: [Principles of writing consistent, idiomatic CSS by Nicolas Gallagher](https://github.com/necolas/idiomatic-css)

#### Property order - Group similar properties

* Declarations should be ordered by structurally important properties (e.g. positioning and box-model) to be declared prior to all others.

The Drupal coding standards, and other people, suggest using alphabetical order, but the drawback is that it separates related properties. For example, position offsets are no longer grouped together and box-model properties can end up spread throughout a declaration block.

Example code:

    .book-admin-form {
        /* Display & Box Model */
        display: block;
        width: 100px;
        height: 100px;
        padding: 10px;
        border: 10px solid #333;
        margin: 0;
        overflow: hidden;
        
        /* Other */
        font-family: helvetica, arial, sans-serif;
        color: #333;
        background: #fff;
        background: linear-gradient(#fff, rgba(0, 0, 0, 0.8));
    }

Source: [Principles of writing consistent, idiomatic CSS by Nicolas Gallagher](https://github.com/necolas/idiomatic-css)

Tip: [CSS Comb](http://csscomb.com) - The Greatest tool for sorting CSS properties in specific order.

#### Exceptions and slight deviations

* Large blocks of single declarations can use a slightly different, single-line format.
* Long, comma-separated property values - such as collections of gradients or shadows - can be arranged across multiple lines in an effort to improve readability and produce more useful diffs. 

Large blocks of single declarations can use a slightly different, single-line format. In this case, a space should be included after the opening brace and before the closing brace.

    .selector-1 { width: 10%; }
    .selector-2 { width: 20%; }
    .selector-3 { width: 30%; }
    
Long, comma-separated property values - such as collections of gradients or shadows - can be arranged across multiple lines in an effort to improve readability and produce more useful diffs. There are various formats that could be used; one example is shown below.
    
    .selector {
        background-image:
            linear-gradient(#fff, #ccc),
            linear-gradient(#f3c, #4ec);
        box-shadow:
            1px 1px 1px #000,
            2px 2px 1px 1px #ccc inset;
    }

Source: [Principles of writing consistent, idiomatic CSS by Nicolas Gallagher](https://github.com/necolas/idiomatic-css)
