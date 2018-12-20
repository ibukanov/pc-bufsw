# pc-bufsw
PC style quick buffer switcher for Emacs

This switches Emacs buffers according to most-recently-used/least-recently-used order using `C-tab` and `C-S-tab` keys. It is similar to window or tab switchers that are available in PC desktop environments or applications.

Installation
------------

### Installing as a package

If your Emacs has package.el (which is automatically the case for Emacs >= 24), you can install pc-bufsw from [MELPA](https://melpa.org/). You can also download [pc-bufsw.el](pc-bufsw.el), open it in Emacs and run `package-install-from-buffer`. After the installation use customization interface for the group `pc-bufsw` to toggle `pc-bufsw` on. To change the keybindings, customize `pc-bufsw-keys`.

### Manual installation

Copy `pc-bufsw.el` to your Emacs load path and add to your Emacs init file:
```
(require 'pc-bufsw)
(pc-bufsw t)
```

Ini file customization
----------------------

To customize key-bindings from the default `Ctrl-Tab` and `Ctrl-Shift-Tab` in the Emacs ini
file set the `pc-bufsw-keys` variable before calling `(pc-bufsw t)`. For example, the following defines `F12`, `F11` keys as buffer switches before actvating `pc-bufsw`. For details, view the documentation for `pc-bufsw-keys`.
```
(setq pc-bufsw-keys '(([f12]) ([f11])))
(pc-bufsw 't)

```

License
-------

This software is in the public domain as stated [here](LICENSE).
