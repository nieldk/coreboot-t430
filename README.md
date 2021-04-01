# coreboot-t430

coreboot V 4.13 rom for thinkpad t430 featuring seabios v. 1.14.0 
Secondary payloads added Nvramcui, Coreinfo, Memtest and Tint

coreboot.rom use the (Intel) vga rom and supports intel wifi cards and bluetooth

seabios time-wait-menu reduced to 1 second only.

Bootsplash added.

me.bin file has been me_cleaned

how to flash:

internally, if already running coreboot and BIOS unlocked:
sudo flashrom -p internal -w coreboot.rom --ifd --image bios -V --noverify-all

If you are not already on an unlocked BIOS, you can use IvyRain (https://1vyra.in/)

Hint: Downgrade Lenovo BIOS to version 2.64 or earlier befor using ivyrain
You can mount the local harddrive, once booted on ivyrain USBstick, and then flash coreboot from the shell it provides.
After exploit is successfull, stop the script (CTRL+C), mount SDA1 (or whichever is you harddrive, with coreboot.rom), and flash using flashrom as above
