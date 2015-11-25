Presentaxa
========

## What's this

Presentaxa is a Beamer presentation theme designed for use with XeTeX. XeTeX is a TeX typesetting engine that can be [thought](http://tex.stackexchange.com/questions/3393/what-is-xetex-exactly-and-why-should-i-use-it) of as standard LaTeX (pdftex) with support for Open Type Fonts. Beamer is a widely used LaTeX class for presentations and slides.

The design and some pieces of code in Presentaxa are based on [Presento template](https://github.com/RatulSaha/presento)


## Installation

Presentaxa is [available as a template](http://papeeria.com/templates#type:preso+presentaxa) 
on online LaTeX editor [Papeeria](http://papeeria.com). You can
just create new documents using this template or download it from Papeeria as a ZIP archive 
and use locally. Provided that you have TeXLive 2015 or some similar distro installed, it should compile 
out of the box.

## Fonts

The fonts in use are:

* [PT Sans Caption](http://www.paratype.com/public/) by Paratype for the presentation title and huge texts. License: SIL Open Font License
* [Lato](http://www.latofonts.com/) (Light)  by Łukasz Dziedzicm for slide titles, License: SIL Open Font License
* [Noto](https://www.google.com/get/noto) Sans by Google for slide body texts. License:  Apache License 2.0
* For small caps we use Idealist Sans Light by Elena Kowalski. License: Creative Commons BY-ND 3.0
* Monospaced text uses [DejaVu Sans Mono](). License: Bitstream Vera Fonts Copyright (http://dejavu-fonts.org)


The fonts and their usage are already baked into the template. However for custom use, the following LaTeX commands (without any arguments) are provided: `\ptsansfont`, `\notosansfont`, `\latolightfont`,`\dejavumonofont`. In order to use small caps, type `\textsc{small caps text}`

## Colors

The color palette is vibrant, bold yet minimal. The following colors can be used with the `\color{colorName}` command.

* `colorlgray`: #FAFAFA (light gray)
* `colordgray`: #795548 (dark gray)
* `colorhgray`: #212121 (heavy dark gray)
* `colororange`: #E65100 (orange)
* `colorgreen`: #009688 (green)
* `colorblue`: #0277BB (blue)

## Custom Macros

See documentation in PresentaxaToolkit.tex

## Changes comparing to Presento
Presentaxa is a major refactoring of [Presento template](https://github.com/RatulSaha/presento)
developed by [Ratul Saha](http://www.ratulsaha.com). Here is a list of changes:

* Presentaxa can be used in a standard Beamer way: `\usetheme{presentaxa}`
* We flattened the structure of files and separated packages defining fonts, colors, utility macros and dependencies
* Some of the originally used fonts didn't have Cyrillic glyphs and were replaced with similar looking fonts
* Custom command and environments were refactored. In particular, itemize environments were replaced with macroses which plug into standard itemizes
* Pie-looking progress indicator was replaced with a growing progress bar at the footer

## Concluding remarks
The typography and design principles have been largly influenced by notable designers around the world. Sincere thanks goes to [Prof. Dr.-Ing. André Miede](http://www.miede.de/) (developer of [Classicthesis](https://code.google.com/p/classicthesis/)), [Robert Bringhurst](http://en.wikipedia.org/wiki/Robert_Bringhurst) (author of 'The Elements of Typographic Style'), [Richard Rutter](http://clagnut.com/) (creator of The Elements of Typographic Style Applied to the Web), Tim Brown (developer of [Modular Scale](http://modularscale.com)), designers at [Google](https://google.com/design) among others.

## License
The original work was not licensed. This work is distributed under Creative Commons BY-SA 4.0

## FAQ

##### How do I change the font sizes?
The spacing and font sizes are carefully designed. Change font sizes by using `\fontsize{size}{leading}\selectfont` only if you are sure of what you are doing.

##### Why does the text in my presentation look pale?
High contrast of black-white is not advisable for presenting with high quality projectors. Thus the background is set to light gray and the text color is set to heavy dark gray. If you are unsure about the quality of the projector and/or the text looks pale, comment out the following in config/presento-config.tex:
```
\setbeamercolor{background canvas}{bg=colorlgray}
\setbeamercolor{normal text}{fg=colorhgray}
```

##### Do I need to download the fonts?
No, the fonts are already present in the fonts/ subfolder. 
