\# Ubuntu 24.10 Desktop – Install Checklist    
\*Project: 23 Linux Distros Installed\*    
\*\*Estimated Time:\*\* \~25 min  

\---

\#\# 0\) Prep    
\- \*\*ISO:\*\* \`ubuntu-24.10-desktop-amd64.iso\` (\~5.28 GB)    
\- \*\*VM Name:\*\* \`2.UBUNTULINUX\`    
\- \*\*RAM:\*\* 4 GB    
\- \*\*CPU:\*\* 1 vCPU    
\- \*\*Storage:\*\* 80 GB VDI (dynamic)    
\- \*\*Display:\*\* VMSVGA, 16 MB Video Memory    
\- \*\*Network:\*\* Bridged Adapter (Intel PRO/1000 MT Desktop)    
\- \*\*Boot Order:\*\* Optical, Hard Disk  

\---

\#\# 1\) Create VM (2 min)    
1\. \*\*New →\*\* Name: \`2.UBUNTULINUX\` → Type: Linux, Version: Ubuntu (64-bit)    
2\. Assign RAM: 4096 MB    
3\. Create VDI → Dynamic → 80 GB    
4\. \*\*Settings:\*\*    
   \- System: Enable VT-x/AMD-V, Nested Paging    
   \- Display: VMSVGA, 16 MB video RAM    
   \- Network: Bridged Adapter    
   \- Storage: Attach ISO  

\---

\#\# 2\) Boot ISO & Start Installer (1 min)    
\- From boot menu: select \*\*Try or Install Ubuntu\*\*  

\---

\#\# 3\) Installer Steps (15 min)  

\*\*Language/Keyboard\*\*    
\- Language: \*\*English (US)\*\*    
\- Keyboard: English (US) default  

\*\*Updates & Other Software\*\*    
\- Checked:    
  \- Install third-party software (graphics, Wi-Fi, proprietary drivers)    
  \- Install support for additional media formats (MP3, MP4, etc.)  

\*\*Disk Setup\*\*    
\- Erase disk and install Ubuntu    
\- No encryption, no LVM  

\*\*Active Directory (AD) Integration\*\* \*(Ubuntu 24.10 feature)\*    
\- Domain: \`bee-lab.local\`    
\- Domain join user: \`administrator\`    
\- Password: entered and validated  

\*\*Time Zone\*\*    
\- Default: New York (EDT)  

\*\*User Account\*\*    
\- Create full name, username, and password    
\- Automatic login: Disabled  

\*\*Installation\*\* \*(\~5–7 min)\*    
\- Copy files, install base system    
\- Install GRUB to \`/dev/sda\`  

\*\*Finish\*\* → Reboot → remove ISO  

\---

\#\# 4\) First Boot (2 min)    
\- GRUB → Ubuntu 24.10 desktop login screen  

\---

\#\# 5\) Post-Install Checks (5 min)  

\*\*Partitions\*\*    
\- \`/dev/sda1\`: \~79 GB ext4 (root, bootable)    
\- \`/dev/sda2\`: swap (size determined by installer; no extended partition, GPT layout)  

\> \*Ubuntu’s Guided Installation in GPT mode creates a single ext4 root partition plus swap (either a swap partition or swapfile, depending on defaults).\*

\*\*System Info\*\*    
\- Ubuntu 24.10 (Oracular Oriole)    
\- GNOME 46.x, Kernel 6.x series    
\- CPU: Intel Core i5-2500S ×1 (vCPU)    
\- RAM: 3.9 GiB usable    
\- Graphics: VMSVGA driver  

\*\*Networking\*\*    
\`\`\`bash  
ip a  
ping \-c 2 ubuntu.com  
\`\`\`  
