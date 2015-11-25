# rpi-jessie

Based on worky by Klaus M Pfeiffer, http://www.kmp.or.at/~klaus/raspberry/build_rpi_sd_card.sh

rpi-jessie will:
  - create, partition and format an image or disk
  - install and configure base debian jessie system with Open SSH server
  - populate image with your files
  - install a first-run script that will re-configure SSH server keys and resize partition to fill the disk on the first run.

### Usage

```sudo ./build_image.sh [block_device]```

block_device is an optional parameter if you want to write directly to a disk instead of an image.
