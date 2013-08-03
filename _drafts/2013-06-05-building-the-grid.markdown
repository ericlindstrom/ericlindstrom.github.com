---
layout: post
title: Building the grid
class: post
featureimage: /media/grid.jpg
---

A good grid system will get you where you need to go, but with much frustration and headache. A great grid system will take you further, happier.

After evaluation all the current grid systems available, I found that they were all too bloated and relied much on learning a new way of coding.

### How I want my markup to look
    <div class="column4">
      <div class="column"></div>
      <div class="column"></div>
      <div class="column"></div>
      <div class="column"></div>
    </div>

isn't that pretty? that's why i'm developing ghostrgrid.

### That's great, but what how is that responsive?
Although there are defaults set, We need to be able to tell these how and when to break. Let's start by defining breakpoint names and paramaters using a mobile first approach.

1. Base (Mobile): Anything less than 600px
2. Small Tablet (Nexus 7): 600px to 767px
3. Large Tablet (iPad): 768px to 999px
4. Desktop: 1000px and up <!-- (to 1239px) -->
<!-- 5. Cinema: 1240px and up (Not implemented, for now) -->

### Responsive markup

It's easiest to think of how we want it to look on desktop, even though we are using a mobile first approach.  So, I have model this structure to "step down" from our largest viewing experince.  

    <div class="gcolumn4 _321">...</div>

you will define "column4" as your desktop, and fill in the rest with a second class. The underscore (_) tells us where to begin. the numbers tell us what happens per breakpoint.
- Desktop: 4 Columns
- Large Tablet: 3 Columns
- Small Tablet: 2 Columns
- Base: 1 Column

If you wanted to "hold" the 4 column grid until the base styling (if below a 3 column grid and below, you can hold that too):

    <div class="gcolumn4 ___1">...</div>
    <div class="gcolumn2 ____">...</div>

breaks available for a 4 column grid: 

    4441, 4321, 4421, 4221
    ___1, _321, __21, _221

I've only used a 4 column grid as an example, these will be available upto a 6 column grid from the start.

