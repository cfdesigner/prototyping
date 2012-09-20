---
layout: design-patterns
title: Progress indicator
template: wide
css: ../css/styles.css
section_class: guide
category: Design patterns
categories: Design pattern
---

Use this near the top of multi-page transactions to help users understand
how many steps there are, 
which step they are on and 
what's involved in each step.


### Example
<div class="pattern-example">
  <div class="inner">

    <nav role="navigation" class="progress-indicator group">
      <span class="visuallyhidden step-count">Step 1 of 4</span>
      <ol class="group">
        <li class="active">Current step</li>
        <li>Step two</li>
        <li>Step three</li>
        <li>Step four</li>
      </ol>
    </nav>

  </div>
</div>

### Code

~~~ html
<nav role="navigation" class="progress-indicator group">
  <span class="visuallyhidden step-count">Step 1 of 4</span>
  <ol class="group">
    <li class="active">Current step</li>
    <li>Step two</li>
    <li>Step three</li>
    <li>Step four</li>
  </ol>
</nav>
~~~


# Dependencies

Include the following in your SCSS to pull in styles for this pattern:

~~~ css
@import "_mixins.scss";
@include progress-indicator;
~~~

The progress-indicator mixin accepts three optional arguments:

`$active-colour`
: The colour of the currently highlighted step (default is white)


`$border-colour`
: The border colour (default is light blue grey)


`$background-colour`
: The background colour (default is cool grey)