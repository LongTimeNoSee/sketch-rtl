# RTL | ⅃TЯ Sketch Plugin#

Designs that include text written in right-to-left languages are often rendered incorrectly.

This happens because some design tools don’t support proper RTL rendering. The result is often embarrassingly illegible gibberish masquerading as Hebrew, Arabic, or Persian text that defeats the purpose of connecting with those audiences. Unless you speak those languages, the mistakes might be hard to spot.

This Sketch plugin takes your designs and automatically creates RTL layouts on new artboards. This should speed up the process of creating RTL designs and improve RTL consistency across your designs.

![example gif](https://cloud.githubusercontent.com/assets/1478273/22186956/fdd78c90-e0b2-11e6-8db7-ffccb17b7a61.gif "Example gif")

## Installation

Simply [download the zipped plugin](https://github.com/devinmancuso/sketch-rtl/releases/download/1.0.0/sketch-rtl-1.0.0.zip), extract it, and double-click to quickly install. This will add a new menu option under Plugins and a new shortcut: ⌘ + Shift + F

There is a demo file included in the zipped directory which you can experiment with. 

## Usage

Select one or more artboards and then press ⌘ + Shift + F or select RTL | ⅃TЯ from the plugin menu.

## Features

At present the RTL plugin has the following features:

* Mirror 1 or more artboards to RTL layout

* Duplicates the artboard(s) and appends _rtl to translated artboard(s) so the plugin is non-destructive

* Shift existing artboards on the same Y position to make room for duplicate artboards

* Detect icon-font and SVG material icons that should be mirrored in RTL

## Flipping Icons

The plugin includes a hashtable of icons which should be flipped in RTL mode. Using this it is able to guess at when an icon should be flipped.

Currently the plugin only supports icon flipping for SVG and material-icon-font

* For SVGs from [material.io/icons](https://material.io/icons/) it looks for the standard layer name, e.g. ic_reply_black_24dp and attempts to match the icon name component "reply" to the list in the hashtable. This method only works if the layer names remain unchanged

* For material-icon-font it gets the value of the TextElement (not the name of the text layer) and attempts to match that to the list in the hashtable.

## Known issues

* An empty groupLayer with the naming convention of an SVG e.g. ic_reply_black_24dp seems to cause the plugin to stop running for the current artboard.

## Note ##

This is not an official Google product.

## Acknowledgments ##

Kudos to Sketch Mate plugin for inspiration on how to cleanly handle artboard repositioning
 
## License ##

[Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0)
