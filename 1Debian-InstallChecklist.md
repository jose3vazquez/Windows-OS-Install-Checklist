\# Debian 12 Cinnamon – Install Checklist    
\*Project: 23 Linux Distros Installed\*    
\*\*Estimated Time:\*\* \~25 min

\---

\#\# 0\) Prep  
\- \*\*ISO:\*\* \`debian-live-12.x-amd64-cinnamon.iso\` (\~3.17 GB)    
\- \*\*VM Name:\*\* \`1.DEBIANLINUX\`    
\- \*\*RAM:\*\* 4 GB    
\- \*\*CPU:\*\* 1–2 vCPUs    
\- \*\*Storage:\*\* 80 GB VDI (dynamic)    
\- \*\*Display:\*\* VMSVGA, 16 MB Video Memory    
\- \*\*Network:\*\* Bridged Adapter (Intel PRO/1000 MT Desktop)    
\- \*\*Boot Order:\*\* Optical, Hard Disk  

\---

\#\# 1\) Create VM (2 min)  
1\. \*\*New →\*\* Name: \`1.DEBIANLINUX\` → Type: Linux, Version: Debian (64-bit)    
2\. Assign RAM: 4096 MB    
3\. Create VDI → Dynamic → 80 GB    
4\. \*\*Settings:\*\*  
   \- System: Enable VT-x/AMD-V, Nested Paging    
   \- Display: VMSVGA, 16 MB video RAM    
   \- Network: Bridged Adapter    
   \- Storage: Attach ISO  

\---

\#\# 2\) Boot ISO & Start Installer (1 min)  
\- From boot menu: select \*\*Start Installer\*\* (not Live system)  

\---

\#\# 3\) Installer Steps (15 min)

\*\*Language/Location/Keyboard\*\*    
\- Choose language → country → keyboard layout  

\*\*Network\*\*    
\- Auto DHCP → Hostname: \`debian\` → Domain: blank  

\*\*User Accounts\*\*    
\- Root password: leave empty → create user \+ password  

\*\*Time Zone\*\*    
\- Select your zone  

\*\*Partitioning\*\*    
\- Guided → Entire disk → All files in one partition    
\- Confirm write to disk  

\*\*Install Base System\*\* \*(\~5–7 min)\*  

\*\*Mirror\*\*    
\- Select country → \`deb.debian.org\` → no proxy  

\*\*Software\*\*    
\- Keep Debian desktop environment \+ Cinnamon \+ standard utilities  

\*\*GRUB Boot Loader\*\*    
\- Yes, install to \`/dev/sda\`  

\*\*Finish\*\* → Reboot → remove ISO  

\---

\#\# 4\) First Boot (2 min)    
\- GRUB → Debian 12 desktop login screen  

\---

\#\# 5\) Post-Install Checks (5 min)

\*\*Partitions\*\*    
\- \`/dev/sda1\`: \~85 GB ext4 (root, bootable)    
\- \`/dev/sda2\`: Extended partition (\~1 GB container)    
  \- \`/dev/sda5\`: 1 GB swap (inside \`/dev/sda2\`)  

\> \*Default Guided Partitioning will create \`/dev/sda1\` (ext4 root) and \`/dev/sda5\` (swap) inside an extended partition.    
This is Debian’s standard behavior in MBR mode.\*

\*\*System Info\*\*    
\- Debian GNU/Linux 12 (bookworm)    
\- Cinnamon 5.6.8, Kernel 6.1.0-29-amd64    
\- CPU: Intel Core i5-2500S ×1 (vCPU)    
\- RAM: 3.8 GiB usable    
\- Graphics: VMware SVGA II (VMSVGA)  

\*\*Networking\*\*    
\`\`\`bash  
ip a  
ping \-c 2 [deb.debian.org](http://deb.debian.org)  
\`\`\`

