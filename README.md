# zdv
Zephyr DAPLink Validation

## Build instructions

Follow the [Zephyr Getting Started Guide](https://docs.zephyrproject.org/2.7.0/getting_started) to setup the build environment. This project is tested using the [GNU Arm Embedded Toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm), you can also look at [the relevant section in Zephyr documentation](https://docs.zephyrproject.org/2.7.0/getting_started/toolchain_3rd_party_x_compilers.html#gnu-arm-embedded).

- Install the toolchain.
- Set `ZEPHYR_TOOLCHAIN_VARIANT` to `gnuarmemb`, and `GNUARMEMB_TOOLCHAIN_PATH` to the toolchain installation directory. Path shall have no whitespace, GNU version 10.x recommended ([GNU Arm Embedded Toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads)).
  ```
  export ZEPHYR_TOOLCHAIN_VARIANT=gnuarmemb
  export GNUARMEMB_TOOLCHAIN_PATH=/usr/local/gcc-arm-embedded/10.3-2021.07
  ```

```
$ virtualenv venv
$ source venv/bin/activate
$ mkdir zdv-workspace
$ cd zdv-workspace
$ export ZEPHYR_TOOLCHAIN_VARIANT=gnuarmemb
$ export GNUARMEMB_TOOLCHAIN_PATH=C:/gnu_embedded/10_2021_10
$ west init -m https://github.com/H4w4k4/zdv
$ west update
$ pip3 install -r zephyr/scripts/requirements.txt
$ make -f zdv/build.mk
```

## Contributors

- [Frank Duignan](https://github.com/fduignan) helped this project get started. See his [Zephyr OS examples for BBC micro:bit v2](https://github.com/fduignan/zephyr_bbc_microbit_v2).
