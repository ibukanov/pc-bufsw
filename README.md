# emacs-pc-bufsw
quick buffer switcher for Emacs according mru/lru order

This switches Emacs buffers according to most-recently-used/least-recently-used order that is similar to one that is often available in Windows or Linux PC applications. The main idea here is that a user chooses two key combinations like C-tab/C-S-tab that switch between buffers according to most or least recently used order. After the final choice is made the last selected buffer becomes the most recently used one.

Installation
------------

Copy `pc-bufsw.el` to your Emacs load path and add to your Emacs ini file:
```
(require 'pc-bufsw)
(pc-bufsw-bind-keys-default)
```

`pc-bufsw-bind-keys-default` binds `C-tab` and `C-S-tab` keys as buffer switchers. To use other keys, call instead `pc-bufsw-bind-keys` like in:
```
(pc-bufsw-bind-keys [f12] [f11])
```
