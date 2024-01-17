# Debian packaging for `fwupd-snap`

This repository contains the packaging for the `fwupd-snap` Debian package.
The purpose of the `fwupd-snap` Debian package is to transition a system
that has the `fwupd` [Debian package](https://tracker.debian.org/pkg/fwupd)
installed to the `fwupd-snap` snap package.

The repository will install the current stable branch of the `fwupd-snap`
snap package from the [Snap Store](https://snapcraft.io/fwupd).

## Building

To build the Debian package, run the following command:

```shell
dpkg-buildpackage -us -uc -b
```

## Installing

To install the Debian package, run the following command:

```shell
sudo apt -i ./fwupd-snap_*.deb
```

This will implicitly install the snap package as well.

## Uninstalling

To uninstall the Debian package and Snap package, run the following command:

```shell
sudo apt remove fwupd-snap
sudo snap remove fwupd
```
