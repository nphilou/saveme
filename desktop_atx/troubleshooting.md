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
