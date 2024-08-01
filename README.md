# Windows-7-for-Thinkpad-T480-or-any-new-hardware

## A windows 7 tutorial for Thinkpad t480 or any new hardware, also for booting via VHD or booting off a external drive!

### need help? or have questions? contact me directly on discord! VelsDie, or email me! velsdie@gmail.com

<h1> NOTE: This guide might not work for you, its tested on the ThinkPad T480, i am NOT RESPONSIBLE for any bricked devices or data loss. </h1>
this iSO was made for an Thinkpad T480 but might work to similar laptops, ONLY FOR INTEL CPU!!!

special thanks to: <a href="https://www.reddit.com/user/SevoosMinecraft/">u/Sevoos</a> for his help, to <a href="https://www.sevenforums.com/members/siw2.html">SIW2</a> for the installation media! and to <a href="https://www.reddit.com/user/gutenprint19/">u/gutenprint19</a> for sharing the driver pack for the t480

<br> the iso comes with usb 3.0 drivers out of the box, which is important to install in a new hardware, the display, wlan, ethernet and more drivers might not work for you out of the box, that is why the drivers are given in the releses. <br>

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

NOTE: doing this will mix your windows 10/11 boot manager with windows 7, which will give 7 the priority, to fix this you can burn a windows 10/11 iso to a usb stick and repair the boot manager.

## Booting from a VHD (Virtual Hard Disk)

### this way is a pretty easy way of booting windows 7 along side windows 10/11 without mixing the EFI folders

### for this you will need a VM and an USB stick with an at least 2gb of space (the VHD will be on the internal ssd)
for vm i suggest orcale vm virtualbox, you can get it from <a href="https://www.virtualbox.org/wiki/Downloads">here</a>

1. First intsall the iso
2. install orcale vm virtualbox (SKIP THIS IF YOU ALREADY HAVE IT OR HAVE OTHER VM WARE)
3. press the windows key + R
4. type diskmgmt.msc and hit enter
5. click on action on top
6. click on create VHD
7. click on browse location and set it on the root of your main drive ( in most cases, C:/ )
8. then enter the space of the VHD (at least 20GB)
9. then leave everything as default and create it
10. after its created go down and select the VHD
11. right click on it and click on initialize disk and select it as MBR
12. Then deatach the vhd
13. now open your VM as admin
14. make a new machine
15. select the iso as the given iso and name the machine as Windows 7 and click on skip unattended installation
16. go to the hard disk option and click on use an existing VHD and select the VHD you just have made
17. now proceed with the installation, but after the first reboot pay attention, after the vm reboots second time, quickly pause the vm and power it off
18. now get your usb stick and plug it in, and if you have anything important there, just back it up
19. install ventoy from here <a href="https://ventoy.net/en/download.html">Ventoy</a>
20. unzip the ventoy file and run the ventoy2disk
21. select your usb and isntall, it will ask you if you are sure twice, just click ok
22. after its done go into your usb stick and make a folder on the root and name it ventoy
23. in the folder that you just made paste this file <a href="https://cdn.discordapp.com/attachments/1262319934202056716/1267514363766640670/ventoy_vhdboot.img?ex=66ad04bd&is=66abb33d&hm=922f6666e768df4a434369ac21b21f6c1ba44fce7aeb787ce1b01ecbd960036c&">ventoy_vhdboot file</a> 
24. 




    
