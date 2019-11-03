# Matrix-boot-screen-for-Linux


Install the plymouth themes tool on Ubuntu. It will create /usr/share/plymouth/themes directory in your system.

> sudo apt install plymouth-themes



Then copy the directory containing the boot theme to the appropriate position

> sudo cp -r matrix /usr/share/plymouth/themes/

Now set the matrix theme as the default by selecting the correct entry (named .../matrix.plymouth)

> sudo update-alternatives --config default.plymouth 

Write settings to boot image:

> sudo update-initramfs -u -k all 
