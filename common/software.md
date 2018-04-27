# Software

## Riot

```
sudo sh -c "echo 'deb https://riot.im/packages/debian/ artful main' > /etc/apt/sources.list.d/matrix-riot-im.list"
curl -L https://riot.im/packages/debian/repo-key.asc | sudo apt-key add -
sudo apt update && sudo apt -y install riot-web
```

## Google Chrome - Chromium

```
sudo apt install apt-transport-https
sudo sh -c 'echo deb https://dl.google.com/linux/chrome/deb/ stable main > /etc/apt/sources.list.d/google-chrome.list'
wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo apt update
sudo apt install google-chrome-stable
sudo apt install chromium
```


## Atom

```
sudo apt install curl
curl -L https://packagecloud.io/AtomEditor/atom/gpgkey | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] https://packagecloud.io/AtomEditor/atom/any/ any main" > /etc/apt/sources.list.d/atom.list'
sudo apt update
sudo apt install atom
```

## Qutebrowser  

1. **buster** in */etc/apt/sources.list.d/buster.list*
```
deb http://ftp.fr.debian.org/debian/ buster main non-free
deb-src http://ftp.fr.debian.org/debian/ buster main non-free

deb http://security.debian.org/debian-security buster/updates main non-free
deb-src http://security.debian.org/debian-security buster/updates main non-free
```

2. Pin-Preference de Buster a <500 dans */etc/apt/preferences*
```
sudo apt install -t buster qutebrowser
```

## Jetbrains toolbox  

tar.gz download at https://www.jetbrains.com/toolbox/app/
tar -zxf in */opt/*
