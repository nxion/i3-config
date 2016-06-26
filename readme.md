# i3 Setup and config from minimal Ubuntu build

####install packages for base system
```sh
i3
i3lock
i3status
xautolock
compton
nitrogen
dmenu
rxvt-unicode
suckless-tools
screenfetch
network-manager
xserver-xorg-input-all 
xserver-xorg-video-all
lxdm
network-manager
build-essential
software-properties-common
unzip
imagemagick
scrot
awk
utils-linux
```
####Download fonts for i3status bar

```sh
# As of wrighting this, the fons package was 4.6.3. Adjust accordingly
wget http://fontawesome.io/assets/font-awesome-4.6.3.zip
```

###Extract fonts to /usr/share
```sh
unzip font-awesome-4.6-3.zip
mv font-awesome-4.6.3 /usr/share/fonts/
```

####Setup fancy lock screen - kudos to @meskarune / https://github.com/meskarune/i3lock-fancy/

```sh
#Clone repo
git clone https://github.com/meskarune/i3lock

#Move script to /usr/local/bin
cd i3lock-fancy
mkdir /usr/local/bin/lock; mv lock lockdark.png lock.png /usr/local/bin/lock/

# Change ownership of the script (not sure if needed yet)
chown root:root /usr/local/bin/lock/lock
```

####Config file location (Ubuntu specific?)
```sh
~/.config/i3/config
~/.config/i3/i3status
```
