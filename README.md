# RTM-Image
Custom Plug & Play Linux-Based USB Image for Raptoreum Mining on dedicated CPU Rigs

## System Requirements
* 64-bit x86 CPU (ARM is not supported)
* UEFI Motherboard Firmware
* Ethernet with DHCP
* 6GB Storage Space on the drive you intend to use

## How to use
1. Download the newest image
2. Flash it onto a storage device using Etcher or Rufus or any other tool you like:
    * Etcher：https://www.balena.io/etcher/
    * Rufus：https://rufus.ie/
3. If you don't see a CONFIG partition then unplug and plug the drive back in
4. edit wallet.txt so that it contains your wallet address
5. edit worker.txt so that it contains your worker name
6. Save, eject and remove the drive
7. Plug in the drive on your mining rig, plug in Ethernet, power and turn it on
8. Choose UEFI OS or UEFI Partition 1 on the drive as your boot device
9. If all things go well then you should be able to see your rig pop up on https://aoipool.net in your dashboard.

## Instructions for moving the drive to another rig
Create a file `reset.txt` in the CONFIG partition before booting up on a new system to reset thread config.

## Support
* Discord：https://discord.gg/fdQ6fNx2yc

## Credits
* Ubuntu：https://ubuntu.com/
* Xmrig：https://github.com/xmrig/xmrig
* blacklist-nouveau：https://github.com/Arondight/xf86-video-nouveau-blacklist/
