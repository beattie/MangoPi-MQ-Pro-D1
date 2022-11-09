# MangoPi-MQ-Pro-D1
Various software projects for MangoPi-MQ-Pro-D1 board (Docker images for buildroot etc...)

[Risc-V Toolchain](https://xpack.github.io/riscv-none-embed-gcc)

* [docker](https://github.com/beattie/MangoPi-MQ-Pro-D1/tree/main/docker): The current [mangopi buildroot](https://github.com/mangopi-sbc/buildroot-mangopi-r) and [Tina-Linux](https://github.com/mangopi-sbc/Tina-linux) on github, do not build on Ubuntu 22.04 so I created a docker image builder for ubuntu 18.04 and packages that will build them.
  * **Tina-Linux** build currently fails in last step with _ERROR: update_boot0 boot0_nand.fex run error_

### Link
* [docker](https://github.com/beattie/MangoPi-MQ-Pro-D1/tree/main/docker)
* [Tina-Linux](https://github.com/mangopi-sbc/buildroot-mangopi-r)
* [Armbian](https://github.com/150balbes/build/tree/risc-v)
