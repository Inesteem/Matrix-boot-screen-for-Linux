# Matrix-boot-screen-for-Linux


Install the plymouth themes tool on Ubuntu. It will create /usr/share/plymouth/themes directory in your system.

> sudo apt install plymouth-themes



Then copy the directory containing the boot theme to the appropriate position

> sudo cp -r matrix /usr/share/plymouth/themes/

Now set the matrix theme as the default by selecting the correct entry (named .../matrix.plymouth)

> sudo update-alternatives --config default.plymouth 

Write settings to boot image:

> sudo update-initramfs -u -k all 


Test installed Boot screen:

> chmod +x ./test-boot-screen.sh

> sudo apt-get install plymouth-x11 

> sudo ./test-boot-screen.sh

There are two screenshots, generated with this script.
The bar on the top will not appear at boot time.


Tested and used on Ubuntu 16.04 / 18.04 

(Use on your own risk. Works for me, but you know, if your PC is on fire after executing this commands... well, bad luck I guess.)

