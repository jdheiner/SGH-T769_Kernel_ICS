SGH-T769_Kernel_ICS
===================

SGH-T769 (Samsung Galaxy Blaze 4G) ICS Kernel

HOW TO BUILD KERNEL 3.0 ICS FOR SGH-T769
========================================

1. How to Build
	- get Toolchain
	download and install arm-eabi-4.4.3 toolchain for ARM EABI.
	Extract kernel source and move into the top directory.

	$ export CROSS_COMPILE=/opt/toolchains/arm-eabi-4.4.3/bin/arm-eabi-
	$ make msm8660-perf_APEX40_USA_TMO_defconfig
	$ make
	
2. Output files
	- Kernel : Kernel/arch/arm/boot/zImage
	- module : Kernel/drivers/*/*.ko
	
3. How to make .tar binary for downloading into target.
	- change current directory to Kernel/arch/arm/boot
	- type following command
	$ tar cvf SGH-T769_Kernel.tar zImage

