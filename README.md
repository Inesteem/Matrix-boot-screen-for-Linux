# Matrix-boot-screen-for-Linux


Install the plymouth themes tool on Ubuntu. It will create /usr/share/plymouth/themes directory in your system.

> sudo apt install plymouth-themes



Then copy the directory containing the boot theme to the appropriate position

> sudo cp -r matrix /usr/share/plymouth/themes/

Now set the matrix theme as the default one by using the below coomand.

> sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/matrix/matrix.plymouth 100

> sudo update-initramfs -u
