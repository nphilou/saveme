# Drivers

## Nvidia (Asus Strix GTX 970)

Add **contrib** and **non-free** to */etc/apt/sources.list*

```
sudo apt update && sudo apt upgrade
sudo apt install nvidia-drivers

```

## WLAN (Broadcom BCM43228 802.11a/b/g/n)

Integrated WLAN card on **Asus Maximus V Formula motherboard**

```
sudo apt install linux-image-$(uname -r|sed 's,[^-]*-[^-]*-,,') linux-headers-$(uname -r|sed 's,[^-]*-[^-]*-,,') broadcom-sta$
sudo modprobe -r b44 b43 b43legacy ssb brcmsmac bcma
sudo modprobe wl

```
