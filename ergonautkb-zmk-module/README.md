# Ergonaut One ZMK Module

This repository contains the board files for the following [Ergonaut](https://ergonautkb.com) keyboards:

- [Ergonaut One](https://github.com/ergonautkb/one/) 
- [Ergonaut One S](https://github.com/ergonautkb/one-s/) 
- [Dao](https://github.com/yumagulovrn/dao-choc-ble/) 

To allow users to build firmware. 
This can be done by adding the module to the west.yml found in your zmk-config's config directory. 
There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the Ergonaut One module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: ergonautkb
      url-base: https://github.com/ergonautkb
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: ergonautkb-zmk-module
      remote: ergonautkb
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.
