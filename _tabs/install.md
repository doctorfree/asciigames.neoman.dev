---
layout: post
icon: fas fa-arrow-circle-down
order: 2
toc: true
post_style: page
---

## Installation

Download the [latest Arch, Debian, or RPM package format release](https://github.com/doctorfree/asciigames/releases) for your platform. If your platform does not support Arch, Debian, or RPM format installs then download the compressed binary distribution archive for your platform and the `Install-bin.sh` script.

### Supported platforms

Asciigames has been tested successfully on the following platforms:

- **Arch Linux 2022.07.01**
  - `asciigames_<version>-<release>-x86_64.pkg.tar.zst`
- **Ubuntu Linux 20.04**
  - `asciigames_<version>-<release>.amd64.deb`
- **Fedora Linux 36**
  - `asciigames_<version>-<release>.x86_64.rpm`
- **Raspberry Pi OS**
  - `asciigames_<version>-<release>.armhf.deb`

### Arch Linux based installation

Arch Linux, Manjaro, and other Arch Linux derivatives use the Pacman packaging
format. In addition to Arch Linux, Arch based Linux distributions include
ArchBang, Arch Linux, Artix Linux, ArchLabs, Asahi Linux, BlackArch,
Chakra Linux, EndeavourOS, Frugalware Linux, Garuda Linux,
Hyperbola GNU/Linux-libre, LinHES, Manjaro, Parabola GNU/Linux-libre,
SteamOS, and SystemRescue.

Install the package on Arch Linux based systems by executing the command:

```shell
sudo pacman -U ./asciigames_1.0.1-2-x86_64.pkg.tar.zst
```

### Debian based installation

Many Linux distributions, most notably Ubuntu and its derivatives, use the
Debian packaging system.

To tell if a Linux system is Debian based it is usually sufficient to
check for the existence of the file `/etc/debian_version` and/or examine the
contents of the file `/etc/os-release`.

Install the package on Debian based systems by executing the commands:

```shell
sudo apt update -y
sudo apt install ./asciigames_1.0.1-2.amd64.deb
```

or, on a Raspberry Pi:

```shell
sudo apt update -y
sudo apt install ./asciigames_1.0.1-2.armhf.deb
```

### RPM based installation

Red Hat Linux, SUSE Linux, and their derivatives use the RPM packaging
format. RPM based Linux distributions include Fedora, AlmaLinux, CentOS,
openSUSE, OpenMandriva, Mandrake Linux, Red Hat Linux, and Oracle Linux.

Install the package on RPM based systems by executing the command

```shell
sudo dnf update -y
sudo dnf localinstall ./asciigames-1.0.1-2.x86_64.rpm
```

### Manual installation

On systems for which the Arch, Debian, or RPM packages will not suffice, install manually by downloading the `Install-bin.sh` script and either the gzip'd distribution archive or the zip'd distribution archive. After downloading the installation script and distribution archive, as a user with sudo privilege execute the commands:

```shell
chmod 755 Install-bin.sh
sudo ./Install-bin.sh /path/to/asciigames_1.0.1-2.<arch>.tgz
or
sudo ./Install-bin.sh /path/to/asciigames_1.0.1-2.<arch>.zip
```

## Removal

Removal of the package on Arch Linux based systems can be accomplished by issuing the command:

```shell
sudo pacman -Rs asciigames
```

Removal of the package on Debian based systems can be accomplished by issuing the command:

```shell
sudo apt remove asciigames
```

Removal of the package on RPM based systems can be accomplished by issuing the command:

```shell
sudo dnf remove asciigames
```

On systems for which the manual installation was performed using the `Install-bin.sh` script, remove Btop manually by downloading the `Uninstall-bin.sh` script and, as a user with sudo privilege, execute the commands:

```shell
chmod 755 Uninstall-bin.sh
sudo ./Uninstall-bin.sh
```
