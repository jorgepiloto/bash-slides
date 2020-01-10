# Bash Slides

This is a simple script written in Bash for slide presentations in terminal.

It is inspired by https://github.com/fxn/tkn.

**It requires terminal which supports 256 colors and formatting.** 
`xterm-256color` should do fine.


## Installation

Clone the repository. 

Required dependencies:
* Bash 4.x + typical GNU utils (tput, head, tail, sed, date, etc.)
* highlight (for code highlighting)

Optional dependencies:
* unclutter (for hiding mouse cursor during presentation)
* Imagemagick (for export to PDF)
* Xorg (for export to PDF)
* xprop (for export to PDF)
* FontAwesome (for nice icons in text)

## Usage

Run the following for example slides:

```
$ ./slides
```

The example slides is a showcase of capabilities and contains slide about controls. 
You can also open generated PDF of the example slides.

For running your own slides, use the following:

```
$ ./slides my-slide-deck-file
```


## Export to PDF

This feature is one big hack.
It only works in X server, not Wayland.
It finds your active window (with a bit of luck it is the terminal emulator window). 
It makes a screenshot of it as PNG, then it moves to the next slide.
In the end it stitches all screenshots in one PDF.


