# Phantom ZMK Module

This repository contains the shield files for the excellent [Phantom](https://github.com/davidphilipbarr/phantom) by David Barr.

**NOTE**: A number of images can be found with one micro-controller face down and the other face up - this is not the case here. **Both micro-controllers should be face down**.

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the phantom module. Example:

```yaml
manifest:
    remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: jonnyirwin
      url-base: https://github.com/jonnyirwin
    projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-keyboards-phantom
      remote: jonnyirwin
      revision: main
    self:
      path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.

## Default Keymap
The default keymap is provided in the module. It is based on the default hummingbird keymap. Here is a visual guide using caksoylar's great [keymap-drawer](https://keymap-drawer.streamlit.app).

![Default Phantom Keymap](https://raw.githubusercontent.com/jonnyirwin/zmk-keyboards-phantom/blob/main/img/keymap.svg)
