# Material Theme for Jupyter Notebook

Custom style sheet for [Jupyter Notebook][1], using Chris Kempson's [Base16][2] color scheme generator based on the beatiful [Material Theme][6] and [Nate Peterson's Material Theme color palette][7]

## Screenshots

#### Original

![Material Theme original screenshot](./screenshots/orginal.png "Material Theme original")

#### Darker

![Material Theme darker screenshot](./screenshots/darker.png "Material Theme darker")

## Installation

Your style sheet will need to be named `custom.css` and
placed in the `~.jupyter/custom/`. So you might grab the `ocean-dark` theme like so:

```sh
wget -O ~/.jupyter/custom/custom.css
https://raw.githubusercontent.com/flekschas/base16-ipython-notebook/master/ipython-2/output/base16-ocean-dark.css
```

## Build

You can edit the templates (located in `./ipython-2/templates` and
`./ipython-3/templates`) by running `make`.

**Custom Theme**

```
cd ./base16-builder && ./base16 -s https://rawgit.com/ntpeters/base16-materialtheme-scheme/master/material-darker.yaml
```

## What happened to the toolbar?

You will probably notice that the top toolbar is gone in these styles. I've hidden it in the
CSS by default, as I find it mostly useless. If you want it back, just
comment out this line:

``` css
div#maintoolbar, div#header {display: none !important;}
```

## Custom fonts

You can use custom fonts in IPython Notebook by uncommenting a block of code at
the top, eg:

``` css
div#notebook, div.CodeMirror, div.output_area pre, div.output_wrapper, div.prompt {
  font-family: 'Inconsolata', monospace !important;
  font-size: 16px;
}
```

## Credits

* Uses Base16 builder by [Chris Kempson][3].
* Based on [base16-codemirror][4] by [Jan T. Scott][5]

[1]: https://github.com/jupyter/notebook
[2]: https://github.com/chriskempson/base16
[3]: https://github.com/chriskempson
[4]: https://github.com/idleberg/base16-codemirror
[5]: https://github.com/idleberg
[6]: https://github.com/idleberg
[7]: https://github.com/ntpeters/base16-materialtheme-scheme
