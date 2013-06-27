# Skeletoast

Skeletoast is the combination of the Skeleton framework's nomenclature
over Toast's inline-block implementation.

I needed a grid system that didn't require clearfix markup since my CMS
didn't give me control over arbitrary markup.

However I was already used to Skeleton and liked it's features and
nomenclature.  Toast was a bit too simple since it didn't support 16
columns, offsets nor nested columns.

The result is a grid system which is:

- fluid - based on percentages not pixels, unlike Skeleton
- responsive - using Toast's simple responsiveness model -
the need for Skeleton's more complex model is less needed because of the
fluidity
- 16-column - using Skeleton's column naming and based on 960px width by
default (can be changed by editing the CSS)
- offsettable - supports offsetting by columns a la Skeleton - this
conflicts with Toast's box-sizing which has been removed
  - note this means that you can't add borders nor padding to blocks since without Toast's box-sizing, they expand the box size and cause wrapping
- nestable - supports a single level of nested columns - no nested-nested columns
  - nested columns only need an additional class on the first, not the last, to remove excess margin - use "leader" class rather than "alpha" (skeleton)
- does not support plurilization of one column ("one columns" is
invalid)
- has no styling other than base font-size (removes both Toast's and Skeleton's styling)
- has Toast's minimal css reset

To learn more about Toast, go to <http://daneden.me/toast>.

To learn more about Skeleton, go to <http://getskeleton.com/>.

## How to use

First, link to skeletoast.css in your HTML document's head:

`<link rel="stylesheet" href="[stylesheet path]/skeletoast.css">`

Then, to use the grid, you'll need a wrap and a grids container.

~~~
<div class="container">
  <div class="grid">
    <div class="twelve columns">
      <p>The left side</p>
    </div>
    <div class="four columns">
      <p>The right side</p>
    </div>
    <div class="sixteen columns">
      <div class="twelve columns">
        <p>Also the left side</p>
      </div>
      <div class="four columns"
        <p>Also the right side</p>
      </div>
    </div>
  </div>
</div>
~~~

