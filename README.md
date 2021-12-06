# RTM-Image
Custom Linux-Based Image for Raptoreum Mining on dedicated CPU Rigs
## 硬體、環境需求 System Requirements
* 64位元CPU 64-bit CPU
* UEFI主機板韌體 UEFI Motherboard Firmware
* 乙太網路連線+DHCP分發IP位置 Ethernet with DHCP
* 6GB儲存空間 6GB Storage Space

## 使用說明 (English Instructions are underneath)
1. 下載最新版映像檔
2. 使用 Etcher 或 Rufus 燒錄至隨身碟上 (或者其他儲存裝置也可以)：
    * Etcher：https://www.balena.io/etcher/
    * Rufus：https://rufus.ie/
4. 如果沒有看到電腦出現 CONFIG 分區的話請重插隨身碟
5. 修改 CONFIG 分區中的 wallet.txt，貼入錢包地址
6. 修改 CONFIG 分區中的 worker.txt，貼入礦機名稱
7. 存檔、退出並移除隨身碟
8. 到礦機上插入隨身碟，接上網路線，插電、開機
9. 選擇隨身的 UEFI Partition 1 作為開機裝置
10. 幾分鐘後至 https://aoipool.net 查詢礦機狀況

## How to use
1. Download the newest image
2. Flash it onto a storage device using Etcher or Rufus:
    * Etcher：https://www.balena.io/etcher/
    * Rufus：https://rufus.ie/
3. If you don't see a CONFIG partition then unplug and plug the drive back in
4. edit wallet.txt so that it contains your wallet address
5. edit worker.txt so that it contains your worker name
6. Save, eject and remove the drive
7. Plug in the drive on your mining rig, plug in Ethernet, power and turn it on
8. Choose UEFI OS or UEFI Partition 1 on the drive as your boot device
9. If all things go well then you should be able to see your rig pop up on https://aoipool.net in your dashboard.

## 換機說明 Instructions for moving the drive to another rig
更換硬體前請先於隨身碟中建立 reset.txt 檔案再到新的電腦上開機，此動作將重置核心配置設定，讓挖礦軟體在新的電腦上重新偵測
Create a file `reset.txt` in the CONFIG partition before booting up on a new system to reset thread config.

## 問題區 Questions (English Ver. underneath)
1. 有計畫加入Wifi支援嗎
    * 沒有 乙太網路穩定很多，而且Linux對於無線網路卡的支援有限

## Questions (English Ver.)
1. Is Wifi support planned?
    * No. Ethernet is much more stable, and Linux has limited support for wifi so supporting it would be a nightmare.

## 支援 Support
* Discord：https://discord.gg/fdQ6fNx2yc

## Credits
* Ubuntu：https://ubuntu.com/
* Xmrig：https://github.com/xmrig/xmrig
* blacklist-nouveau：https://github.com/Arondight/xf86-video-nouveau-blacklist/
