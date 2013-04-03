---
layout: blog_post
title: General Format
categories : [format]
---

#### Minimise the use of element selectors 

Selectors that contain elements tightly coupled the CSS to specific markup. It is not a safe assumption that the semantics of the content will never change so authors should prefer classes which exist independent of markup and create more flexible CSS.

Source: [SMACSS on modules](http://smacss.com/book/type-module)

#### Do not use location based selectors

A location based selector is a selector that changes a modules appearance based on its location (content area, side bar, header etc).  Where a module has different appearances it is better to use a module subclass.  If the appearance and/or content is very different it would be better to use a different module

Source: [OOCSS, slide 20](http://www.slideshare.net/stubbornella/object-oriented-css)

#### Do not use ID's in CSS Selectors

It is never safe to assume there will only ever be one of something on a page so do not use ID's for CSS.  Id's are much better used as javascript hooks so use them for this instead.

Source: [SMACSS on layout](http://smacss.com/book/type-layout)

#### Use dashes to separate words

CSS properties do not use underscores or camel case, they use dashes.  Do the same with classes 

### Selectors

#### Include a single space before the opening brace of a ruleset.

Example code:
    
    .book-navigation .page-next {
    }
    
    .book-navigation .page-previous {
    }
    

A blank line should be placed between each group, section, or block of multiple selectors of logically related styles.

#### Multiple selectors should each be on a single line, with no space after each comma. 

    #forum td.posts,
    #forum td.topics,
    #forum td.replies,
    #forum td.pager {

#### Selectors should be 4 or less levels deep

Long complex selector chains spawn specificity wars and are slower for the browser to evaluate.  Its unlikely you _need_ to use a selector more than 4 levels deep.  If it is, consider adding additional classes to the markup to enable a shorter selector length.

Long selector chains also have an impact on the page load, however it is minor. In other words, consider selector performance but don’t waste too much time on it.

Source: [SMACCS - Depth of Applicability](http://smacss.com/book/applicability)

Source: [SMACCS - Selector Performance](http://smacss.com/book/selectors)


