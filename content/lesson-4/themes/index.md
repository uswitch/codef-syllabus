---
title: "How Themes Work"
date: 2020-06-10T15:49:55+01:00
order: 2
draft: true
---
# Hugo themes
As you may have come to understand by now, a _theme_ is nothing more than a collection of layouts and some CSS.  It usually gets you a good starting point, and you can tweak and customise step by step, but your finished site often looks nothing like the original theme.

You won't see any actual CSS code in this particular theme.

This is because Ananke uses a CSS library called [Tachyons](https://tachyons.io/).

## Styling your site

_Tachyons_ is one of a few CSS libraries designed to make common, repetitive styling easy. Most CSS deals with setting font sizes, element widths, heights, centering or aligning text, dealing with colour, and other menial tasks like that. Writing code for all of this would get tiring, so some nice people on the Internet have written all this for us, and made it available publicly and for free.

You use Tachyons by simply assigning classes to your HTML. The `f3` and `near-black` classes we saw in an example earlier are defined by Tachyons. `f3` sets the font-size to be the [third largest](http://tachyons.io/docs/typography/scale/). `near-black` sets the [colour](https://tachyons.io/docs/themes/skins/).

You can use Tachyons to customise your site, by changing the `class` fields of your templates. E.g., to make all text left-aligned, you'd give the corresponding HTML element the [`tl` class](http://tachyons.io/docs/typography/text-align/) (you might need to remove an existing `tc` class).

You now have the full set of tools to make your site look exactly the way you want.

If you find a place that you don't like, you can copy that template or partial into the site's `layouts/` folder, and then tweak it by adjusting the HTML, changing the classes to style it, or both.

# Further reading

## CSS

### MDN Intro

### Box model
https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model
