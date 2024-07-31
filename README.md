# Windows-7-for-Thinkpad-T480-or-any-new-hardware

## A windows 7 tutorial for Thinkpad t480 or any new hardware, also for booting via VHD or booting off a external drive!

### need help? or have questions? contact me directly on discord! VelsDie, or email me! velsdie@gmail.com

<h1> NOTE: This guide might not work for you, its tested on the ThinkPad T480, i am NOT RESPONSIBLE for any bricked devices or data loss. </h1>
this iSO was made for an Thinkpad T480 but might work to similar laptops, ONLY FOR INTEL CPU!!!
<br>
special thanks to: <a href="https://www.reddit.com/user/SevoosMinecraft/">u/Sevoos</a> for his help, to <a href="https://www.sevenforums.com/members/siw2.html">SIW2</a> for the installation media! and to <a href="https://www.reddit.com/user/gutenprint19/">u/gutenprint19</a> for sharing the driver pack for the t480

## So before i start with the guide, this is tested on the thinkpad t480, with an intel cpu, it will not work any computer with a amd cpu, please give feedback on the other models of laptops

# INSTALLATION GUIDE

## install the iso from
here: <a href="https://github.com/VelsDie/Windows-7-for-Thinkpad-T480-or-any-new-hardware/releases/tag/iSO">iSO</a>
## install the thinkpad t480 drivers from
here: <a href="https://github.com/VelsDie/Windows-7-for-Thinkpad-T480-or-any-new-hardware/releases/tag/DRIVERS">Drivers</a>

## the guide is seperated into three types: normal installation, booting from VHD, booting from an external drive (hdd/ssd)

### Normal installation 

you will need: a pc running windows, an usb stick (minimum 8GB of space)

1. install the iso
2. get Rufus from here <a href="https://rufus.ie/downloads/">Rufus</a>
3. open rufus and select the iso
4. then select the targeted USB
5. select the image option as standart windows setup
6. select partition scheme as GPT
7. leave rest as default
8. start and wait for the burning
9. after its done, close rufus and remove the usb
10. press windows key + R
11. type diskmgmt.msc
12. select a partition/disk that you want to install windows in (if you have an partition made for it skip this step)
13. right click that partition/disk and select shrink volume
14. enter the size of the partition you want (minimum 20GB) IN MB (exmpl. 20000mb for 20gb)
15. click ok and wait for it to complete
16. select the new unlocated partition and right click on it and select new simple volume
17. and then just fast forward it, make sure its NTFS
18. now power off the laptop and plug in your usb
19. boot into bios via f1 (or f2,esc or any key for your pc)
20. Open the Security tab, and then select Secure Boot menu. Select Secure Boot, and then select Disabled, press f10 to save and exit
21. enter the boot menu via f12 (in thinkpads, on other models could be diffrent)
22. and boot from the usb
23. now you can just proceed with the installation, make sure you install on the correct partition
24. after its done just install the drivers from the driver pack, put them on a usb or go into your main partition and find it (for thinkpads only, some drivers like the wlan,display,audio might work on other laptops)
25. now you are all done!

## Booting from a VHD (Virtual Hard Disk)

### this way is a pretty easy way of booting windows 7 along side windows 10

### for this you will need a VM
i suggest orcale vm virtualbox, you can get it from <a href="https://www.virtualbox.org/wiki/Downloads">here</a>

1.




    
