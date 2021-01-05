# Kitty Theme Picker

A simple interactive plugin (kitten) for the [kitty][] terminal emulator.
The plugin allows previewing and picking from a list of user colorschemes.

## Installation

Copy `theme_picker.py` to `~/.config/kitty/`. e.g.

```
cp theme_picker.py ~/.config/kitty/
```

Add the following lines to `kitty.conf`:

```
include colors.conf
map ctrl+shift+t kitten theme_picker.py --theme_path ~/.config/kitty/colors/
```

You can manually invoke the kitten with:

```
kitty @ kitten theme_picker.py --theme_path ~/.config/kitty/colors/
```

## Themes

Currently kitty-theme_picker searches the `~/.config/kitty/colors` folder by default for theme `.conf` files. If this folder does not exist on your system, please create it. An example theme should look like this:

``` conf
# Tab bar colors and styles
active_tab_foreground       #efac36
active_tab_background       #382927
inactive_tab_foreground     #ac7f5c
inactive_tab_background     #382927
inactive_border_color       #493734
active_border_color         #7daf9c
bell_border_color           #cc4232

# special
foreground   #e6e1c4
background   #382927
cursor       #7daf9c

# black
color0       #493734
color8       #ac7f5c

# red
color1       #cc4232
color9       #ef5d32

...
```

[kitty]: https://github.com/kovidgoyal/kitty
