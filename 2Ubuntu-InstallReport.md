# Ubuntu 24.10 Desktop – Installation Report
*Project: 23 Linux Distros Installed*  
**Estimated Installation Time:** ~25 minutes  

## ISO and Virtual Machine Setup
**ISO used**: `ubuntu-24.10-desktop-amd64.iso` (~5.28 GB)  
**VM Name**: 2.UBUNTULINUX  
**RAM**: 4 GB  
**CPU**: 1 vCPU  
**Storage**: 80 GB VDI (dynamic)  
**Display**: VMSVGA, 16 MB Video Memory  
**Network**: Bridged Adapter (Internet access during install)  
**Boot Order**: Optical, Hard Disk  

## Installation Process
**Boot selection**: Selected “Try or Install Ubuntu” at boot, then chose “Install Ubuntu”.  

**Language, location, and keyboard**: Configured for English (US) region and keyboard layout.  

**Network**: Configured via DHCP; Internet connectivity available during installation.  

**Active Directory integration**: Joined an AD domain during setup using administrator credentials (credentials validated; domain name omitted by request).  

**User setup**: Created a standard user account with password.  

**Time zone**: Set to New York (EDT).  

**Partitioning**: Guided – Erase disk and install Ubuntu.  

**Partition layout**: `/dev/sda1` (~79 GB ext4 root, bootable), `/dev/sda2` (extended), `/dev/sda5` (~1 GB swap inside extended).  

**Base system install**: Took about 5–7 minutes.  

**Package selection**: Ubuntu desktop (GNOME) with third-party drivers and additional media codecs enabled.  

**Bootloader**: GRUB installed to `/dev/sda`.  

## First Boot
**Login**: GRUB menu appeared, system booted into Ubuntu 24.10 GNOME login screen.  

**System details**: Ubuntu 24.10 (Oracular Oriole), GNOME 46.x, Kernel 6.x series.  

**Hardware assigned**: Intel Core i5-2500S (vCPU), 3.9 GiB usable RAM, VMSVGA graphics.  

**Networking verification**: Confirmed with `ip a` and `ping -c 2 ubuntu.com`.  
