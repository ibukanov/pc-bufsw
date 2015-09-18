# pc-bufsw
PC style quick buffer switcher for Emacs

This switches Emacs buffers according to most-recently-used/least-recently-used order using `C-tab` and `C-S-tab` keys. It is similar to window or tab switchers that are available in PC desktop environments or applications. 

Installation
------------

Copy `pc-bufsw.el` to your Emacs load path and add to your Emacs init file:
```
(require 'pc-bufsw)
```

Alternatively, run `(package-install-from-buffer ".../pc-bufsw.el")` on the downloaded file to install `pc-bufsw` as a package.

By default this binds `C-tab` and `C-S-tab` keys as buffer switchers. To use other keys, set the values of `pc-bufsw-key-most` and `pc-bufsw-key-least` variables either via the customize group `pc-bufsw` or directly in your init file. For example, the following define `F12`, `F11` keys as buffer switches:
```
(setq pc-bufsw-key-most '([f12]))
(setq pc-bufsw-key-least '([f11]))
```
These calls must precede the above `(require 'pc-bufsw)` or package initialization.
