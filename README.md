# Windows-7-for-Thinkpad-T480-or-any-new-hardware

## A windows 7 tutorial for Thinkpad t480 or any new hardware, also for booting via VHD or booting off a external drive!

### need help? or have questions? contact me directly on discord! VelsDie, or email me! velsdie@gmail.com

<h1> NOTE: This guide might not work for you, its tested on the ThinkPad T480, i am NOT RESPONSIBLE for any bricked devices or data loss. </h1>
this iSO was made for an Thinkpad T480 but might work to similar laptops
Please note that Windows 7 should not be used as a main/daily OS on a modern hardware, this is for experimental reasons and for the nostalgia, if you want this on a old computer as an main OS, please try Linux, distros like Linux Mint are lightweight,modern and easy to use, if you need windows, you can use Tiny10 till October 14, 2025, or Tiny11, if you want a modern OS but like the frutiger aero, chcek out href="https://classic7.lol">Classic7</a> which is windows 10 reskinned to look like windows 7.

special thanks to: <a href="https://www.reddit.com/user/SevoosMinecraft/">u/Sevoos</a> for his help, to <a href="https://www.sevenforums.com/members/siw2.html">SIW2</a> for the installation media! and to <a href="https://www.reddit.com/user/gutenprint19/">u/gutenprint19</a> for sharing the driver pack for the t480

<br> the iso comes with usb 3.0 drivers out of the box, which is important to install in a new hardware, the display, wlan, ethernet and more drivers might not work for you out of the box, that is why the drivers are given in the releses. <br>

## So before i start with the guide, this is tested on the thinkpad t480, please give feedback on the other models of laptops

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
20. Open the Security tab, and then select Secure Boot menu. Select Secure Boot, and then select Disabled, after that go into the boot section and enable CSM support, press f10 to save and exit
21. enter the boot menu via f12 (in thinkpads, on other models could be diffrent)
22. and boot from the usb
23. now you can just proceed with the installation, make sure you install on the correct partition
24. after its done just install the drivers from the driver pack, put them on a usb or go into your main partition and find it (for thinkpads only, some drivers like the wlan,display,audio might work on other laptops other than that, you will have to find them yourself) 
25. now you are all done!

NOTE: doing this will mix your windows 10/11 boot manager with windows 7, which will give 7 the priority, to fix this you can burn a windows 10/11 iso to a usb stick and repair the boot manager, and you have to enable CSM support everytime you boot into windows 7, i recommend keeping it off when you are not booting into windows 7

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
24. after that power off your laptop with the usb plugged in
25. go into bios via f1 (for the t480 its f1, if youre trying this on a diffrent model it could be f2, or esc or something else)
26. Open the Security tab, and then select Secure Boot menu. Select Secure Boot, and then select Disabled, then go into boot section and enable CSM support, press f10 to save and exit
27. enter the boot menu via f12 (in thinkpads, on other models could be diffrent)
28. boot from the usb
29. after that the ventoy menu should appear
30. press f2 and enter your main drive/partitionl
31. and find the vhd you made
32. enter it and it should boot
33. and you are done! windows 7 should proceed normally with the installation, after its done downloading, for t480 users just use the driver pack i gave the link of amd install the drvers (for non t480 users, you will have to find the drivers yourself). note that the wlan and ethernet drivers do not come out of the box.

this will not mix your efi partitions and its a safe way to use windows 7, only bad side of its that you have to use the USB everytime you want to boot into windows 7, and you will have to enable CSM support everytime you want to boot, i recommend keeping it off when you are not booting or using windows 7

## Booting windows 7 off an external drive (hdd/ssd)

### this way of booting windows is great if you dont have much space, dont want to mix your efi folders, make use of an sata hdd/sdd and more

for this you will need an external drive that is via usb, or an sata to usb adapter, NOTE that this method needs a clean disk, so back up your important data from the disk, you can put them back after the installation, this method can work via big enough usb or sd card too, this method only works with VHD!

1. first install the iso
2. plug in your external drive
3. then install WinToUSB from here <a href="https://www.easyuefi.com/wintousb/">WinToUSB</a>
4. install WinToUSB setup and finsh it
5. open the programe
6. select the Windows To Go option
7. select the given iso
8. select your external drive
9. select the partition scheme as MBR
10. select the installation mode as VHD and enter the size
11. leave the rest as default and start the process
12. after its done turn off your laptop with the external drive plugged in
13. go into bios via f1 (for the t480 its f1, if youre trying this on a diffrent model it could be f2, or esc or something else)
14. Open the Security tab, and then select Secure Boot menu. Select Secure Boot, and then select Disabled, after that go into the boot section and enable CSM support, press f10 to save and exit
15. enter the boot menu via f12 (in thinkpads, on other models could be diffrent)
16. boot from the external drive
17. and you are done! windows 7 should proceed normally with the installation, after its done downloading, for t480 users just use the driver pack i gave the link of amd install the drvers (for non t480 users, you will have to find the drivers yourself). note that the wlan and ethernet drivers do not come out of the box.

the only down side of this is that you have to keep your external drive on while using windows 7, other than that it will run little slower because it is booting and working from an USB.

## And thats it, if you have any problems or errors (errors after installation or after the boot (NON BSOD) fix could be found on youtube or google, or forums), contact me from discord or email, or here, if you are intrested in hackintoshing your thinkpad t480, you can find my full guide and pre made working efi here: (if you are reading this, the repo is not made yet, stay tuned!)

if you see this repo unprofessnioal, please be understanding, this is my first github repo, and if you see/spot any writing mistakes, please report them to me.

thats all from me, i hope you have a great morning/day/afternoon/evening/night :)




    
