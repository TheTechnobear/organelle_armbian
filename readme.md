    apt-get install git
    mkdir armbian
    cd armbian/
    git clone --depth 1 https://github.com/armbian/build

   ./compile.sh config-default.conf BOARD=cubox-i RELEASE=stretch BRANCH=next BUILD_DESKTOP=no KERNAL_ONLY=no KERNEL_CONFIGURE=no > mybuild.sh
  output is in : output/images/Armbian_5.38_Cubox-i_Debian_stretch_next_4.14.15.img 
