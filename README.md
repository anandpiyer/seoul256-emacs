[![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=plastic)](https://github.com/anandpiyer/seoul256-emacs/blob/master/LICENSE)
#Seoul256 for Emacs 

Seoul256 for Emacs is an Emacs theme port of [**seoul256 color scheme for vim**](https://github.com/junegunn/seoul256.vim/) by Junegunn Choi. This is a work in progress.

## Screenshots
### Dark
![Seoul256-Emacs-Dark](seoul256-emacs-dark.png?raw=true "Dark Variant")
### Light
![Seoul256-Emacs-Light](seoul256-emacs-light.png?raw=true "Light Variant")

## Installation & Usage
### Manual
Download and save the following file into your custom theme directory (e.g., `~/.emacs.d/themes`):

* [seoul256-theme.el](https://raw.githubusercontent.com/anandpiyer/seoul256-emacs/master/seoul256-theme.el)

Make sure Emacs knows about your custom theme directory. You may do this by adding something like the following in your init file: 

```el
(add-to-list 'custom-theme-load-path "~/.emacs.d/themes")
```

Now you can load the theme using `M-x load-theme RET seoul256`.

## Customization
### Color Variants
Like the original, this port offers different background colors. To change the background, use the variable `seoul256-background` before loading the theme, e.g.,
 
```el
(setq seoul256-background 237)
(load-theme 'seoul256 t)
```
The variant of the theme (dark or light) is determined by this variable. Dark variants range from 233 to 239 and light variants range from 252 to 256. By default, the theme uses a dark variant. 

### Overriding Default Colors
If you don't like the default colors, you can override them by defining new colors in `seoul256-override-colors-alist` variable before loading the theme:

```el
(setq seoul256-override-colors-alist
'((16 . "#CCCCCC")
  (200  . "#F6F6F6"))
(load-theme 'seoul256 t)
```
