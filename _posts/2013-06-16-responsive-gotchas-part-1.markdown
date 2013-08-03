---
layout: post
title: Responsive Gotchas Part 1
class: responsive-gotchas
---

A few things, just because they are becoming extremely relevant.

- Only `<br/>` if you really mean it.
- `&nbsp;` is your best friend to prevent orphans

And a general styling note... when creating styling for your `h1`, `h2`, etc.  add classes in a situation that you want to use the styling but you do not want to use a second h1.

    h1, .h1 { 
      font-size:1.8em; 
    }
