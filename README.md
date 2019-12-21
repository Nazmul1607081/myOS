**Please copy paste below command to install necessary tools**

sudo apt-get install g++

sudo apt-get install binutils

sudo apt-get install libc6-dev-i386

sudo apt-get install grub-legacy

sudo apt-get install virtualbox

sudo apt-get install xorriso

sudo apt-get install nano


**Then download my OS folder and delete _swp , kernel.o , loader.o , mykernel.bin , mykernel.isofiles  and edit kernel.cpp file as you like** 

**Then copy paste the following commands**

make kernel.o

make loader.o

make mykernel.bin

sudo nano /boot/grub/grub.cfg

**Then open a file you should go to the end of the file and paste the below code**

menuentry 'My Operating System' {
  multiboot /boot/mykernel.bin
  boot
}

**Then press ctrl+o and then press ctrl+x enter then paste below command**

make install

## now restart your virtual box and press f12 and see your os on grub menu select it and you see your output.
Thanks




