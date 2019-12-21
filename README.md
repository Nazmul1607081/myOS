#1 Please copy past below command to install necessary tools

sudo apt-get install g++
sudo apt-get install binutils
sudo apt-get install libc6-dev-i386
sudo apt-get install grub-legacy
sudo apt-get install virtualbox
sudo apt-get install xorriso
sudo apt-get install nano

#2 Then download my OS folder and delete _swp , kernel.o , loader.o , mykernel.bin , mykernel.isofiles  and edit kernel.cpp file as you like 

#3 Then copy past this commands

make kernel.o
make loader.o
make mykernel.bin
sudo nano /boot/grub/grub.cfg

#4 Then open a file you should go to the end of the file and past the below code

menuentry 'My Operating System' {
  multiboot /boot/mykernel.bin
  boot
}

#5 Then press ctrl+o and then press ctrl+x enter then past below command

make mykernel.iso

## now restart your virtual box and press f12 and see your os on grub menu select it and you see your output.
Thanks




