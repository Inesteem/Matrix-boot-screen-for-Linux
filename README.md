
# Preface

Use at your own risk. Do not mess with boot images if you don't understand the implications of a broken boot image. 

If you get an error while booting after you followed the instructions below (something like 'kernel needs to be loaded first') use another kernel version (Advanced Options for Ubuntu) instead of using the first grub option Ubuntu.
After booting rebuild the broken build image. 

In general: Before messing with boot images (update-initramfs ...) you should save them (they are located in the /boot dir). Do not update all boot images  (-k all option) at once.

If your system is on fire, consider reading something like: https://linoxide.com/linux-how-to/fixing-broken-initrd-image-linux/

Have fun :)

# Matrix-boot-screen-for-Linux


Install the plymouth themes tool on Ubuntu. It will create /usr/share/plymouth/themes directory in your system.

> sudo apt install plymouth-themes



Then copy the directory containing the boot theme to the appropriate position

> sudo cp -r matrix /usr/share/plymouth/themes/

Now set the matrix theme as the default by selecting the correct entry (named .../matrix.plymouth)

> sudo update-alternatives --config default.plymouth 

Write settings to boot image:

> sudo update-initramfs -u 


Test installed Boot screen (does not work for Ubuntu 18.04+):

> chmod +x ./test-boot-screen.sh

> sudo apt-get install plymouth-x11 

> sudo ./test-boot-screen.sh

There are two screenshots, generated with this script.
The bar on the top will not appear at boot time.


Tested and used on Ubuntu 16.04, 18.04 and 20.04 (but the test script does not work for all)


