# rpi-jessie

Debian Jessie image builder for Raspberry Pi2.

Based on worky by Klaus M Pfeiffer, http://www.kmp.or.at/~klaus/raspberry/build_rpi_sd_card.sh

rpi-jessie will:
  - create, partition and format an image or disk
  - install and configure base debian jessie system with Open SSH server
  - download rpi-update which will install the nescessary firmware and bootloader for RPi2
  - install a first-run script that will re-configure SSH server keys and resize partition to fill the disk on the first run.

### Requirements

Debian Jessie host with the following packages installed:

```binfmt-support qemu qemu-user-static debootstrap kpartx lvm2 dosfstools```

### Usage

```sudo ./build_image.sh [block_device|image_file]```

You can pass block_device (/dev/mmcblk0) to create the image directly on a card, or specify image_file you would like to create. If neither is given, an image file called rpi_basic_jessie_$(date).img will be created. You can write this image to a card using dd or other tools.