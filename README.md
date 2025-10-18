# Linux-Laptop-Startup-Guide
This is my personal linux gaming laptop guide, made for me.  My laptop is the Asus ROG Strix Scar 18 with RTX5090.  These are processes I follow, this may not work for everyone.  follow these instructions at your own risk.

#Missing ASUS functionality.
**1) Drivers**
  While the stock drivers are fine for most everything, I've found the best gaming experience it is best to purge the included nvidia drivers and then reinstall.  Changing this alone DOUBLED my FPS in some games, like path of exile 2

 1. disable dGPU or set iGPU as primary.
 2. open terminal
    ```sudo apt purge ^nvidia-.*```
    ```sudo apt autoremove```
    ```sudo update-initramfs -u```
3. reboot
4. open "Software & Updates"
5. goto Additional Drivers tab
6. Select the 2nd to last one, for me.
    Using NVIDIA driver (open kernel) metapackage from nvidia-driver-580-open (proprietary)
