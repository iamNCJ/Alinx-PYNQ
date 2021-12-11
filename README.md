# Alinx-PYNQ
 PYNQ board spec for Alinx boards

## PYNQ Verion
 2.7.0, with petalinux 2020.2 as backend

## Board List
 - AXU2CGA
 - AXU3EG (Removed eMMC Support for PYNQ to Boot)

> **Notes**: 
> 1. Alinx boards might suffer from USB3.0 error in petalinux kernel 2020.2, downgrade the kernel to 2020.1 version if USB3.0 matters to you.
> 2. Currently the base overlay is empty and just to pass the PYNQ build process. Please use your custom overlay.
> 3. For those who still want to use the 8GB eMMC, mpdify the source code of PYNQ to change the root to /dev/mmcblk1p2 in boot args. (Modifying `system-user.dtsi` is useless due to the dummy build stages in PYNQ)
