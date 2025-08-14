{\rtf1\ansi\ansicpg1252\cocoartf1561\cocoasubrtf610
{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Debian 12 Cinnamon \'96 Installation Report\
*Project: 23 Linux Distros Installed*  \
**Estimated Installation Time:** ~25 minutes  \
\
## ISO and Virtual Machine Setup\
**ISO used**: `debian-live-12.x-amd64-cinnamon.iso` (~3.17 GB)  \
**VM Name**: 1.DEBIANLINUX  \
**RAM**: 4 GB  \
**CPU**: 1\'962 vCPUs  \
**Storage**: 80 GB VDI (dynamic)  \
**Display**: VMSVGA, 16 MB Video Memory  \
**Network**: Bridged Adapter (Internet access during install)  \
**Boot Order**: Optical, Hard Disk  \
\
## Installation Process\
**Boot selection**: Started the installer directly from the ISO boot menu.  \
\
**Language, location, and keyboard**: Configured for preferred region and layout.  \
\
**Network**: DHCP auto-configured, hostname set to `debian`, domain left blank.  \
\
**User setup**: No root password set, created a new user account with password.  \
\
**Time zone**: Selected according to location.  \
\
**Partitioning**: Guided \'96 Use Entire Disk option.  \
\
**Partition layout**: `/dev/sda1` (~85 GB ext4 root, bootable), `/dev/sda2` (extended), `/dev/sda5` (~1 GB swap inside extended).  \
\
**Base system install**: Took about 6\'967 minutes.  \
\
**Package selection**: Debian desktop environment with Cinnamon and standard utilities.  \
\
**Bootloader**: GRUB installed to `/dev/sda`.  \
\
## First Boot\
**Login**: GRUB menu appeared, system booted into Debian 12 Cinnamon login screen.  \
\
**System details**: Debian GNU/Linux 12 (bookworm), Cinnamon 5.6.8, Kernel 6.1.0-29-amd64.  \
\
**Hardware assigned**: Intel Core i5-2500S (vCPU), 3.8 GiB usable RAM, VMware SVGA II (VMSVGA) graphics.  \
\
**Networking verification**: Confirmed with `ip a` and `ping -c 2 deb.debian.org`. }