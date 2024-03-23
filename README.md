Bootloader built using assembly and C programming language. 
Prerequisites

The project requires a Unix-like environment. If you are using Windows, there are various ways of setting one up (WSL, a Linux virtual machine, Cygwin, MSYS2).

 you need the following tools:

    make
    nasm
    Open Watcom
    qemu-system-x86 for testing
    bochs-x bochsbios vgabios for debugging
    your preferred text editor

Installing Open Watcom

    Download the latest build at  https://github.com/open-watcom/open-watcom-v2/releases
    Run the installer with sudo (the downloaded file is executable)
    When prompted for what components to install, select "Selective installation" and enable "Include 16-bit compilers"
    If you installed the 64-bit version, in Makefile and src/bootloader/stage2/Makefile modify the CC16 and LD16 variables to point to /usr/bin/watcom/binl64/wcc and /usr/bin/watcom/binl64/wlink. If you modified the installation path, set the correct paths.

Build instructions

    run make

Running with qemu

    run ./run.sh

Debugging with bochs
Used to debugging and check if the registers are working as intended 
    run ./debug.sh
