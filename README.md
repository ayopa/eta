# About

You can use Eta to build a distribution based on Arch Linux. The main goals are

* Support for custom packages. The sources are made available as a git
submodule and the build is incremental. Thus it makes code development
convenient.
* Support for fully atomic and safe upgrades. This is made possible by
[OSTree](https://wiki.gnome.org/OSTree). Note that support for traditional
package management is currently not a goal.

# Git repository layout

The build scripts works on a well known repository layout.

* source/ directory. It contains git submodules with the sources of each custom
package.
* build/ directory. Each subdirectory is a standard Arch Linux package, containing a PKGBUILD file, following the [VCS guidelines](https://wiki.archlinux.org/index.php/VCS_PKGBUILD_Guidelines).
* conf/pacman.conf. The pacman configuration used to compose the distribution.
* conf/eta.conf. The Eta configuration, currently supporting the following
variables
    * OSNAME. The name of the OS, required by OSTree.
    * MODULES. A list of custom modules.
    * PKGS. A list of official Arch Linux packages.
    * ORIGIN_URL. The URL of OSTree repository.

# Build

You need to run the commands inside the git repository. First build the custom
packages

    sudo eta-build

Compose the system root and commit it to the OSTree repository

    sudo eta-commit

Build a raw image of the system, suitable to copy on a USB drive

    sudo eta-pack
