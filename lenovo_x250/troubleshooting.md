# Troubleshooting

## Tap to click

```
sudo nano /usr/share/X11/xorg.conf.d/40-libinput.conf
Option "Tapping" "on"
```

## Tearing

```
lspci -nn | egrep -i "3d|display|vga"
sudo mkdir /etc/X11/xorg.conf.d
sudo nano /etc/X11/xorg.conf.d/20-intel.conf

Section "Device"
   Identifier  "Intel Graphics"
   Driver      "intel"
   Option      "TearFree"    "true"
EndSection
```
