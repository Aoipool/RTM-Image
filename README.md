# RTM Mining Image for USB
Custom Plug & Play Linux-Based USB stick Image for Raptoreum Mining on dedicated CPU Rigs

## System Requirements
* 64-bit x86 CPU (ARM is not supported)
* UEFI Motherboard Firmware
* Ethernet with DHCP (WiFi is not supported)
* 6GB or larger drive as boot device for mining rig (**All contents of this drive WILL be erased**)

## How to use
1. Download the newest image from the releases page
2. Flash it onto a drive using Etcher or Rufus or any other tool you like:
    * Etcher：https://www.balena.io/etcher/
    * Rufus：https://rufus.ie/
3. If you don't see a CONFIG partition then unplug and plug the drive back in
4. Put your wallet address in wallet.txt
5. Put your rig name into worker.txt
6. Save, eject and remove the drive
7. Plug in the drive on your mining rig, plug in Ethernet, plug in power and turn it on
8. Choose UEFI OS or UEFI Partition 1 or ubuntu on the drive as your boot device in your motherboard BIOS
9. If all things go well then you should be able to see your rig pop up on https://aoipool.net in your dashboard.

## Instructions for moving the drive to another rig
Create a file `reset.txt` in the CONFIG partition before booting up on a new system to reset thread config.
Moving directly to another rig without resetting may result in suboptimal hashrate.

## Support
* Discord：https://discord.gg/fdQ6fNx2yc

## Credits
* Ubuntu：https://ubuntu.com/
* Xmrig：https://github.com/xmrig/xmrig
* blacklist-nouveau：https://github.com/Arondight/xf86-video-nouveau-blacklist/
