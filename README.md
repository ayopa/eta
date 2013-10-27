# About

You can use Eta to build a distribution based on Arch Linux. The main goals are

* Support for custom packages. The sources are made available as a git
submodule and the build is incremental. Thus it makes code development
convenient.
* Support for fully atomic and safe upgrades. This is made possible by
[OSTree](https://wiki.gnome.org/OSTree). Note that support for traditional
package management is currently not a goal.
