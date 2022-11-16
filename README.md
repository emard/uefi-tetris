# UEFI-Tetris 

Tetris game for UEFI, based on [bare-metal-tetris](https://github.com/programble/bare-metal-tetris) 
This fork allows clockwise and counter-clockwise rotation
(original allowed only clockwise).

# Installation

Copy EFI executable to EFI VFAT boot partition
(should be done after each recompile).

    cp tetris.efi /boot/efi/EFI/tetris/

# Run from UEFI shell

fs1: is example of EFI filesystem name where tetris is,
it could be fs0: or similar

    fs1:
    cd EFI/tetris
    tetris.efi

# Run from GRUB menu

Make GRUB menu entry to start from boot menu
(should be done only once).

    cp 40_custom /etc/grub.d/
    update-grub

## Screenshot 

![screenshot](https://raw.githubusercontent.com/a1ive/uefi-tetris/master/screenshot.png) 

## Requirements 

- make 

- gnu-efi 

- gcc 
  