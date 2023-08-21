---
layout: post
icon: fas fa-info-circle
order: 2
toc: true
post_style: page
---

## Building asciigames from source

Asciigames can be compiled, packaged, and installed from the source code
repository. This should be done as a normal user with `sudo` privileges:

```shell
# Retrieve the source code from the repository
git clone https://github.com/doctorfree/asciigames.git
# Enter the asciigames source directory
cd asciigames
# Compile the asciigames components and create an installation package
./mkpkg
# Install asciigames and its dependencies
./Install
```

These steps are detailed below.

### Clone asciigames repository

```shell
git clone https://github.com/doctorfree/asciigames.git
cd asciigames
```

**[Note:]** The `mkpkg` script in the top level of the asciigames
repository can be used to build an installation package on all supported
platforms. After cloning, `cd asciigames` and `./mkpkg`. The resulting
installation package(s) will be found in `./releases/<version>/`.

### Install packaging dependencies

asciigames components have packaging dependencies on the following:

On Debian based systems like Ubuntu Linux, install packaging dependencies via:

```shell
sudo apt install dpkg
```

On RPM based systems like Fedora Linux, install packaging dependencies via:

```shell
sudo dnf install rpm-build rpm-devel rpmlint rpmdevtools
```

### Build and package asciigames

To build and package asciigames, execute the command:

```shell
./mkpkg
```

On Debian based systems like Ubuntu Linux, the `mkpkg` scripts executes
`scripts/mkdeb.sh`.

On RPM based systems like Fedora Linux, the `mkpkg` scripts executes
`scripts/mkrpm.sh`.

On PKGBUILD based systems like Arch Linux, the `mkpkg` scripts executes
`scripts/mkaur.sh`.

### Install asciigames from source build

After successfully building and packaging asciigames with either
`./mkpkg`, install the asciigames package with the command:

```shell
./Install
```
