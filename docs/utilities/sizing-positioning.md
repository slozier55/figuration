---
layout: docs
title: Sizing & Positioning
group: utilities
---

Gain a little more control over your layout.

## Contents
{:.no_toc}

* ToC goes here
{:toc}

## Widths/Heights

Easily make an element as wide as its parent using the `.width-100` utility class, which sets `width: 100%`.

{% example html %}
<img class="width-100" data-src="holder.js/200px100?outline=yes&text=Width%20%3D%20100%25" alt="Width = 100%">
{% endexample %}

There is also a `.height-100` utility class, which sets `height: 100%`.  However, it probabaly won't work the way you think it does.  [This article](http://webdesign.about.com/od/csstutorials/f/set-css-height-100-percent.htm) has a few details on working with precentage heights.

## Fixed Positioning

The `.position-f-t` class can be used to easily position elements at the top of the viewport and make them as wide as the viewport. **Be sure you understand the ramifications of fixed-position elements within your project.** Here's how the class is defined:

{% highlight scss %}
.position-f-t {
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  z-index: $zindex-navbar-fixed;
}
{% endhighlight %}

## Vertical Row Alignment

Give some vertical alignment,  using `display: table;` to keep items in a full width row.  Child items need to be defined with `.valign-item` in order to receive alignment.

{% example html %}
<div class="valign-top">
    <div class="valign-item">
        <a href="#">View more in teacher's guide</a> |
        <a href="#">Common Core alignment</a>
    </div>
    <div class="valign-item text-right">
        <button type="button" class="btn btn-primary btn-lg">Continue</button>
    </div>
</div>

<div class="valign-middle">
    <div class="valign-item">
        <a href="#">View more in teacher's guide</a> |
        <a href="#">Common Core alignment</a>
    </div>
    <div class="valign-item text-right">
        <button type="button" class="btn btn-primary btn-lg">Continue</button>
    </div>
</div>

<div class="valign-bottom valign-sample">
    <div class="valign-item">
        <a href="#">View more in teacher's guide</a> |
        <a href="#">Common Core alignment</a>
    </div>
    <div class="valign-item text-right">
        <button type="button" class="btn btn-primary btn-lg">Continue</button>
    </div>
</div>
{% endexample %}
