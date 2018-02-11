 Armbian config files for Organelle

 I'll expand on build instructions but for now refer to armbian.com

basically clone armbian build , then copy the files from this report into that repo.

included is a kernel config file, i think this has to be moved manually to
./cache/sources/linux-mainline/linux-4.14.y/.config


    apt-get install git
    mkdir armbian
    cd armbian/
    git clone --depth 1 https://github.com/armbian/build

   ./compile.sh config-default.conf BOARD=cubox-i RELEASE=stretch BRANCH=next BUILD_DESKTOP=no KERNAL_ONLY=no KERNEL_CONFIGURE=no > mybuild.sh
 
  output is in : output/images/Armbian_5.38_Cubox-i_Debian_stretch_next_4.14.15.img 

there is a organelle_build.sh


primary goal is:
- clean build for Organelle
- build includes:
filesystems
mother host
factory patches

all necessary dependent software - primarily pure data, python 

