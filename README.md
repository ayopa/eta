# About

Eta is the Agora build system.

# How to build

First of all install eta

    makepkg -i

Then clone the agora repository

    git clone https://github.com/ayopa/agora.git
    cd agora

Build the packages

    sudo eta-build

Construct the root filesystem and commit it

    sudo eta-commit

Create the OS image

    sudo eta-pack

Copy it to an USB drive

    sudo dd if=out/agora.img of=/dev/sd[X] bs=1M
