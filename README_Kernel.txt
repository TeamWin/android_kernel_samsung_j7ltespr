################################################################################

1. How to Build
	- get Toolchain
		From android git server , codesourcery and etc ..
		 - arm-eabi-4.8
		
	- edit Makefile
		edit "CROSS_COMPILE" to right toolchain path(You downloaded).
		  EX)  CROSS_COMPILE= $(android platform directory you download)/android/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/bin/arm-eabi-
		  Ex)  CROSS_COMPILE=/usr/local/toolchain/arm-eabi-4.8/bin/arm-eabi-		// check the location of toolchain

	- make
		$ mkdir $(pwd)/out
    $ make -C $(pwd) O=$(pwd)/out msm8929_sec_defconfig VARIANT_DEFCONFIG=msm8929_sec_j7_spr_defconfig SELINUX_DEFCONFIG=selinux_defconfig
    $ make -C $(pwd) O=$(pwd)/out

2. Output files
	- Kernel : out/arch/arm/boot/zImage
	- module : drivers/*/*.ko

3. How to Clean	
		$ make clean
################################################################################
