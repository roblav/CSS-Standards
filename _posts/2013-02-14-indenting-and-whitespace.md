---
layout: blog_post
title: 2. Indenting and Whitespace
---

* Use an indent of 2 spaces, with no tabs.
* Lines should have no trailing whitespace at the end.

Files should be formatted with \n as the line ending (Unix line endings), not \r\n (Windows line endings).

All text files should end in a single newline (\n). This avoids the verbose "\ No newline at end of file" patch warning and makes patches easier to read since it's clearer what is being changed when lines are added to the end of a file.

Tip: configure your editor to "show invisibles". This will allow you to eliminate end of line whitespace, eliminate unintended blank line whitespace, and avoid polluting commits.

Source: [Principles of writing consistent, idiomatic CSS by Nicolas Gallagher](https://github.com/necolas/idiomatic-css)

Source: [Drupal Coding Standards](http://drupal.org/coding-standards)