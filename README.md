# pc-bufsw
PC style quick buffer switcher for Emacs

This switches Emacs buffers according to most-recently-used/least-recently-used order using `C-tab` and `C-S-tab` keys. It is similar to window or tab switchers that are available in PC desktop environments or applications.

Installation
------------

### Installing as a package

If your Emacs has package.el (which is automatically the case for Emacs >= 24), you can install pc-bufsw from [MELPA](https://melpa.org/). You can also download [pc-bufsw.el](pc-bufsw.el), open it in Emacs and run `package-install-from-buffer`. After the installation use customization interface to set `pc-bufsw-keys-enable` in the group `pc-bufsw` to true and apply and save it. This binds `C-tab` and `C-S-tab` keys as buffer switchers. To change the keybindings, customize `pc-bufsw-keys`.

### Manual installation

Copy `pc-bufsw.el` to your Emacs load path and add to your Emacs init file:
```
(require 'pc-bufsw)
(pc-bufsw-default-keybindings)
```

This activates the default `C-tab` and `C-S-tab` keybindings. To use other keys, explicitly set keys to `pc-bufsw-mru` and `pc-bufsw-lru` functions. For example, the following define `F12`, `F11` keys as buffer switches:
```
(require 'pc-bufsw)
(global-set-key [f12] 'pc-bufsw-mru)
(global-set-key [f11] 'pc-bufsw-lru)
```

You can also use such manual bindings after installing the package, but then make sure that the packages are initialized before using pc-bufsw symbols using either explicit `(package-initialize)` call in your ini file or with `after-init-hook` or similar:

```
(package-initialize)
...

(global-set-key [f6] 'pc-bufsw-mru)
(global-set-key [f5] 'pc-bufsw-lru)
```

License
-------

This software is in the public domain as stated [here](LICENSE).
