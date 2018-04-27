# Troubleshooting

## Playerctl is missing
https://github.com/acrisci/playerctl/releases

```
wget https://github.com/acrisci/playerctl/releases/download/v0.6.0/playerctl-0.6.0_amd64.deb
sudo dpkg -i playerctl-0.6.0_amd64.deb
```

## Play/Pause keys
Configuration for *~/.config/i3/config*
```
bindsym XF86AudioPause exec playerctl play-pause
bindsym XF86AudioStop exec playerctl stop
```

Useful :
```
sudo showkey -k
xmodmap -pke
```

## Drives mounting
> not authorized to perform operation

```
sudo nano /etc/polkit-1/localauthority/50-local.d/55-storage.pkla
```

add :
```
[Storage Permissions]
Identity=unix-group:plugdev
Action=org.freedesktop.udisks.filesystem-mount;org.freedesktop.udisks.drive-eject;org.freedesktop.udisks.drive-detach;org.freedesktop.udisks.luks-unlock;org.freedesktop.udisks.inhibit-polling;org.freedesktop.udisks.drive-set-spindown
ResultAny=yes
ResultActive=yes
ResultInactive=no
```

```
sudo usermod -a -G plugdev <your username>
```
*It works, I don't know why*

## Screen teering in browsers
> tearing causes tears

1. Open **nvidia-settings**
2. Go to **X Server Display Configuration**
3. Enable **Force Composition Pipeline**

*It works, I don't know why*
