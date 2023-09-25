# Unermux

[![DISCORD](https://img.shields.io/badge/Chat-On%20Discord-738BD7.svg?style=for-the-badge)](https://discord.gg/Xaqkdeh)

## What's This?

This is a distro that allows you to install Ubuntu in your termux application without a rooted device

## Updates

**• Updated to ubuntu 23.04**

## Important

**• If you have to use ubuntu in termux with a x86/i\*86 architecture or prefer ubuntu 19.10 you can use this branch -> https://github.com/MFDGaming/ubuntu-in-termux/tree/ubuntu19.10**

**• If you get an error message that says "Your kernel has too old" you have to uncomment the line that reads "command+=" -k 4.14.81"" (remove the # that is located in front of the line) in the "startubuntu.sh" file**

### Installation steps

1. Update termux: `apt-get update && apt-get upgrade -y`
2. Install proot: `apt-get install proot -y`
3. Install proot-distro: `apt-get install proot-distro -y`
4. Enable storage: `termux-setup-storage`
5. Go to HOME folder: `cd`
6. Install X11-Repo + TigerVNC + VNCServer + VNC: `pkg install x11-repo && pkg install tigervnc`
7. Install Xhost: `pkg install xorg-xhost`
8. Install VNC Server or You Cannot Use Termux Desktop
9. Enter This Command After You Install VNC Server: `vncserver -geometry 1280x720 -listen tcp :1 && DISPLAY=:1 xhost +`
10. Turn Off Dark Mode Cuz Termux Desktop has Problem: Black Screen
11. Install Treble And Check Your System
12. on Android 12 And Late Android Version, Just Disable Signal 9 (Same as Android 9 Pie) or Phantom Process Killer (Same as VPhoneGaGa) (Google And YouTube)
13. on Older Android Version And Android 12 (AOSP), Install Android 13 Instead (Google + YouTube)
14. on Touchwiz, Samsung Experience, Old One UI And One UI 4, Install One UI 5 Instead (Google + YouTube)
15. on Older MIUI Version And MIUI 13, Install MIUI 14 Instead (Google + YouTube)
16. on Older ColorOS/Realme UI/OxygenOS And ColorOS 12/Realme UI 3/OxygenOS 12, Install ColorOS 13/Realme UI 4/OxygenOS 13 Instead (Google + YouTube)
17. on Older FunTouch OS And FunTouch OS 12, Install FunTouch OS 13 Instead (Google + YouTube)
18. Install Ubuntu (Non-Desktop): `proot-distro install ubuntu`
19. Install Ubuntu (GNOME Desktop): `apt update && apt install gnome-session-flashback -y && apt install gnome-terminal ubuntu-wallpapers dbus-x11 -y`
20. Install Nano: `pkg install nano`
21. Create a File with Nano: `nano /usr/local/bin/vncstart`
22. Follow This Nano:
#!/bin/sh


rm -rf /run/dbus/pid
dbus-daemon --system dbus-launch
DISPLAY=:1
$HOME/.vnc/xstartup
24. Enter This Command: `chmod +x /usr/local/bin/vncstart`
25. Create XStartup File: `mkdir $HOME/.vnc && nano $HOME/.vnc/xstartup`
26. Follow This Nano:
#!/bin/sh


export
XKL_XMODMAP_DISABLE=1
unset SESSION_MANAGER
unset
DBUS_SESSION_BUS_ADDRE
SS
[ -x /etc/vnc/xstartup ] &&
exec /etc/vnc/xstartup [ -r $HOME/.Xresources ] &&
xrdb $HOME/.Xresources xsetroot -solid grey gnome-panel &
metacity &
gnome-flashback &
panel &
23. Now Start GNOME Desktop: vncstart
24. Use VNC Server: localhost:1

## If You Don't Work, Use Post Issue

Post Issue Let You Solve Problem And It's was Based on Reddit And Quora (GitHub)
Once You Fix a Problem, VNC Server And Termux Desktop Can Be Work
