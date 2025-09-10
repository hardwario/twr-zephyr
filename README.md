# Zephyr for Tower

This repository shows how Zephyr RTOS can be used on the HARDWARIO Tower Core
module. It contains all the required drivers and devicetree definions along
with various samples. Additonally the wireless button application has been
reimplemented on top of Zephyr in a backwards compatible manner.

## Initialization

A new Zephyr workspace can be created based on this repository using the following commands:

```
west init -m git@github.com:hardwario/twr-zephyr.git --mr main twr
cd twr
west update
```

If you already have an existing west workspace for your project, this repository can be added
as a dependency in `west.yml`. Example:

```yaml
  projects:
    - name: twr
      url: https://github.com/hardwario/twr
      revision: main
    ...
```

> **NOTE:** this project depends on a custom fork of Zephyr hosted at
> [marekmaskarinec/zephyr](https://github.com/hardwario/zephyr), which mainly
> adds support for the stm32l083 soc. The fork is not being actively kept up-to-date.

---

Made with &#x2764;&nbsp; by [**HARDWARIO a.s.**](https://www.hardwario.com/) in the heart of Europe.
