# Install-Ubuntu

# Udroid Ubuntu Installer & Fixer for Android

**Run full Ubuntu Desktop (XFCE/GNOME) on Android using Termux and Udroid. This repository provides scripts to automate the setup and fix common audio/display issues, but also includes full manual instructions below.**

# Features

**•One-Click Setup:** Installs dependencies (X11, Audio) automatically.
**•Auto-Fix Script:** Clears "Access Denied" or "Display Locked" errors.
**•Audio Support:** Enables PulseAudio for sound in Linux (fixes Firefox audio).
**•No Root Required.**

# Option 1: Automatic Setup
**If you just want to get it running quickly, use the included scripts.**

1.Open Termux and clone this repo:
```
pkg install git -y
git clone https://github.com/cloudaii/ubuntu-on-android.git
cd ubuntu-on-android
chmod +x setup.sh launch.sh
```
2.Run the installer:
```
./setup.sh
```
**3.To Start Ubuntu (Every time): Run the launch script. It automatically fixes audio and display locks.**

```
./launch.sh
```
# manually install 
**install dependencies**
open Termux 
```
pkg update && pkg upgrade -y
```
# install udroid (ubuntu)
**run official Installer**

```
. <(curl -Ls https://bit.ly/udroid-installer)
```
# login udroid 
```
udroid login jammy:xfce4
```
```
udroid login jammy: gnome
```
# install udroid 
```
udroid install jammy:xfce4
```
```
udroid install jammy: gnome
```

# install this
```
pkg install x11-repo -y
```
```
pkg install termux-x11-nightly -y
```

# start display server
```
termux-x11 :1  -ac &
```
# start desktop 
```
export DISPLAY=:1
```
```
startxfce4 &
```

