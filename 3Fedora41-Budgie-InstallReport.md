# Fedora 41 Budgie – Installation Report
*Project: 23 Linux Distros Installed*  
**Estimated Installation Time:** ~22 minutes  

## ISO and Virtual Machine Setup
**ISO used**: `Fedora-Workstation-Live-x86_64-41_Budgie.iso` (~2.3 GB)  
**VM Name**: 3.FEDORALINUX  
**RAM**: 4 GB  
**CPU**: 2 vCPUs  
**Storage**: 80 GB VDI (dynamic)  
**Display**: VMSVGA, 16 MB Video Memory  
**Network**: Bridged Adapter (Internet access during install)  
**Boot Order**: Optical, Hard Disk  

## Installation Process
**Boot selection**: Selected “Start Fedora-Workstation-Live” from GRUB menu.  

**Language, location, and keyboard**: English (US) language, US keyboard layout.  

**Live session**: Entered Fedora 41 Budgie desktop live environment before launching installer.  

**Installation destination**: Selected the only available virtual disk (80 GB). Automatic partitioning chosen.  

**Partition layout**: `/dev/sda1` (EFI System Partition, 600 MB, FAT32), `/dev/sda2` (root, ~79 GB, ext4).  

**Time zone**: Set according to local region.  

**User setup**: Created one local user with administrator privileges and password. Enabled automatic login.  

**Base system install**: Installation took ~8 minutes from live environment.  

**Bootloader**: GRUB2 installed to EFI partition.  

## First Boot
**Login**: Automatic login into Fedora 41 Budgie desktop environment.  

**System details**: Fedora Linux 41 (Budgie Desktop 10.8.1), Kernel 6.8.x series.  

**Hardware assigned**: Intel Core i5-2500S (2 vCPUs), 3.8 GiB usable RAM, VMware SVGA II (VMSVGA) graphics.  

**Networking verification**: Confirmed with `ip a` showing bridged adapter interface, and `ping -c 2 fedoraproject.org` successful.  
