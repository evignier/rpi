# Raspberry Pi CLI OS flash
## Requirements
- SD card
- Linux system with USB port
- USB to SD adapter
- Keyboard
- MicroHDMI to HDMI adapter
- Monitor or TV
- Raspberry Pi
## Steps
- Download the [OS image](https://www.raspberrypi.com/software/operating-systems/)
`wget <url>`
- Decompress the file
`unxz <file.img.xz>`
- Check current devices
`lsblk`
- Connect SD Card to the USB to SD adapter and then to the Linux system USB port
- Run `lsblk` again and Identify the device
- Unmount it
`umount /dev/sda1`
- Flash the image
`sudo dd if=path/to/your/image.img of=/dev/sda bs=4M status=progress` 
- Ensure all data is written to the SD before removing it
`sync`
- Eject SD card
`eject /dev/sda`
- Plug SD card and the keyboard to the Raspberry Pi
- Connect HDMI cable to the TV and the Raspberry Pi and power on
