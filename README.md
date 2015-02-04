SkinnyTip JavaScript Tooltip Library
========================

![alt text](http://www.ebrueggeman.com/sites/www.ebrueggeman.com/files/images/project_preview_skinnytip.png "SkinnyTip Example")

### Overview

SkinnyTip is a lightweight and easy-to-use JavaScript library for tooltip
creation. SkinnyTip does not require additional third party libraries or
frameworks to function, and is usable across all modern browsers.

### History

The first version SkinnyTip was written in 2006 by Elliott Brueggeman to 
allow easy creation of tooltips on sites and applications. The library was 
modernized and rewritten first in 2007, and again in 2015 when it was open-
sourced under the MIT License. Please visit 
http://www.ebrueggeman.com/skinnytip for more information.

### Why *This* Tooltip Library?

I was implementing a [Foundation Library](http://foundation.zurb.com/docs/components/tooltips.html) tooltip (which is built on jQuery) on a web application, but encoutered 
a limit to the number of tooltips I could put on the page before Firefox 
crashed - around 150. I pulled up and rewrote this library, which I had 
originally written long ago for the same effective purpose. Using SkinnyTip, 
and within reason given, there is no effective limit to the number of tooltips 
you can place on a page. Here's an example page with 10000 tooltips. 

SkinnyTip is fast, easy-to-setup, doesn't require external libraries.

### Setup

To use SkinnyTip, you need to include the library within the head and 
include the initialization snippet within the body.

Include this script in the page head:

```html
<script type="text/javascript" src="skinnytip.js"></script>
```

Include this script in the body, preferably at the end before the `</body>` tag:

```html
<script type="text/javascript">SkinnyTip.init();</script>
```

### Usage

To enable a tooltip on an element, add the class `skinnytip` and the following 
data attributes:

| Attribute | Required | Description |
| ---- |----| ----|
| data-text | Required | The contents of the toopltip. |
| data-title | Optional | The title over the contents of the tooltip. |
| data-options | Optional | A string of options to customize the tooltip. See [Advanced Usage](#advanced-usage) below for more details. |


#### Examples - *[See these examples in action](http://ebtest2.ebrueggeman.com/skinnytip/sample.html)*

```html
<span class="skinnytip" data-text="This is the contents of the tooltip">
	Span that triggers a tooltip
</span>
```

```html
<a class="skinnytip" data-text="This is the contents of the tooltip">
	Link that triggers a tooltip
</a>
```

```html
<span class="skinnytip" data-text="This is the contents of the tooltip" 
data-title="This is the title of the tooltip">
	Span that triggers a tooltip with a title and text
</span>
```

## Advanced Usage

You can add the `data-options` data attribute and specify comma-separared option and value pairs to customize the appearance and behavior of a tooltip.

| Option | Default Value | Description |
| ---- |----| ----|
| width | 300px | The width of the tooltip box in pixels.  Note that the value is in the css style of formatting. You must include px or other unit when specifying this option. |
| border | 2px | The border size in pixels. Note that the value is in the css style of formatting. You must include px or other unit when specifying this option. A 0 value means no border. |
| borderColor | #FC6 | The border color, which is also the background color of the title text, if a title is included. #FFCC66 = orange yellow. |
| backColor | #FFC | The background color of the tooltip box. #FFFFCC = light yellow. |
| textColor | #000 | The color of the tooltip text. #000 is black. |
| titleTextColor | #000 | The color of the tooltip title text. #000 is black. |
| fontFace | Arial, Helvetica, Sans-Serif | The font family specification of both the tooltip text and title |
| fontSize | 14px | The font size of the tooltip text. Note that the value is in the css style of formatting. You must include px or other unit when specifying this option. |
| titleFontSize | 14px | The font size of the tooltip title. Note that the value is in the css style of formatting. You must include px or other unit when specifying this option. |
| titlePadding | 1px | Padding inside the title area, if there is a title specified. Note that the value is in the css style of padding formatting. You must include px or other unit when specifying this option. |
| textPadding | 1px 3px | Padding inside the tooltip text area. Note that the value is in the css style of padding formatting, so it is set to 1px padding on the bottom and top, and 3px padding on the right and left. You must include px or other unit when specifying this option. |
| xOffset | 15 | Number of pixels the tooltip is horizontally right of the cursor. You do not need to specify the 'px' unit when specifying. |
| yOffset | 15 | Number of pixels the tooltip is vertically below of the cursor. You do not need to specify the 'px' unit when specifying. |

#### Advanced Usage Examples - *[See these examples in action](http://ebtest2.ebrueggeman.com/skinnytip/sample.html)*

```html
<span class="skinnytip" data-text="This is the contents of the tooltip" 
data-options="borderColor: #333, backColor: #333, width: 150px, 
textPadding: 10px, textColor: #FFF">
	Span that triggers a tooltip with a title and text
</span>
```

```html
<span class="skinnytip" data-text="This is the contents of the tooltip. This 
is the contents of the tooltip. This is the contents of the tooltip" 
data-title="Observations" data-options="borderColor: #3F3, backColor: #EFE">
	Span that triggers a tooltip with a title and text
</span>
```

And the kitchen sink example:

```html
<span class="skinnytip" data-text="This is the contents of the tooltip" 
data-title="This is the title!" data-options="width: 200px, border: 1px, 
borderColor: #000, backColor: #CCC, textColor: #00F, titleTextColor: #0F0, 
fontFace: verdana, fontSize: 12px, titleFontSize: 12px, titlePadding: 10px, 
textPadding: 10px, xOffset: 30, yOffset: 30">
	Span that triggers a tooltip with a title and text
</span>

```
