---
title: Wiping Drives Securely on Linux
date: 2026-04-04
---

## Wiping Drives Securely on Linux


How to check if the its currently used

lsblk
#PROVIDE EXAMPLE OF OUTPUT#

unmont the drtives it mounted
sudo umount /dev/sdX#

wipe all parittions
sudo wipefs -a /dev/sdX*

confirm ti worked
lsblk

turn on drive
sudo hdparm -Y /dev/sdX



HDDs
```bash
sudo dd if=/dev/urandom of=/dev/sda# bs=1M status=progress
```

SSDs
Due  to urandom being slow on ssd due to 
```bash
sudo dd if=/dev/zero of=/dev/sda# bs=1M status=progress
```

SD Cards
Due to SOC/SDCS and hwo they will they will tyr to them from them by reading raw bytes from some non stanrded sectos int he ebginnginf of thecard eg sunxi/Allwinner at LBA 16, RockChip at LBA 64. So the following needs to be done

```bash
dd if=/dev/zero of=/dev/sdX bs=4M count=1
```

## How to wipe on MacOS

Researcgh difference and theory behind
sgdisk --zap-all /dev/sdX
shred -v -z /dev/sdX