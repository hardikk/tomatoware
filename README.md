tomatoware
==========

Tomatoware is a project that creates a native compiling environment for Tomato firmware supported routers.  
In fact, tomatoware is firmware agnostic, and should work with dd-wrt and other mipsel based firmwares.

Downloads for the project can be found at http://lancethepants.com/files

This project is called tomatoware because it originally began using the TomatoUSB toolchain, and was designed to use the libraries already found in TomatoUSB firmware.
I soon found that the TomatoUSB toolchain is somewhat antiquated, and insufficent for the purpose of this project.
I decided to use a more up-to-date toolchain provided from the entware project. http://code.google.com/p/wl500g-repo/

This project allows you to compile applications natively on your mipsel device.
I wanted this to mimic the 'buildroot' package available from optware.
I really like the idea of freeing users to compile code on their own, instead of being soley dependant on package managers.

To be safe, I'm going to say that this is NOT compatible with entware. 
While is uses the same toolchain, many of the libraries are newer.

Running 'make' will compile the toolchain if it is not already installed, and then will compile tomatoware.

Currently I'm compiling this on Ubuntu Server 12.04 and 12.10. I've recently moved to a Debian 7 system, and just have compiled my own entware toolchain as noted above
The following packages should be sufficient to compile this software.  These are probably more than necessary, but libraries I've needed anyway. Some of these are invalid for debian systems, just remove those packages and it should work just fine.

sudo apt-get -y install autoconf automake automake1.7 automake1.9 bash binutils bison build-essential bzip2 cvs diffutils doxygen dpkg-dev file flex g++ g++-4.4 gawk gcc gcc-multilib gettext git-core gperf groff-base intltool libbz2-dev libc6:i386 libc6-dev libcurl4-openssl-dev libgc-dev libglib2.0-dev libslang2 libtool make patch perl pkg-config python python-all python-dev python2.7-dev lib32z1 lib32z-dev libc6 libexpat1-dev libffi-dev libgdbm-dev libncurses-dev  libreadline6-dev libssl-dev libsqlite3-dev libstdc++6-4.4-dev libxml-parser-perl m4 sed shtool sqlite subversion tar texinfo tk-dev zlib1g zlib1g-dev unzip
