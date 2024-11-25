dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X.


Requirements
------------
In order to build dwm you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.

patches added:
actualfullscreen
alpha
moveresize
preserveonrestart
swallow
alwayscenter
scratchpads
hide vacant tags
notitle
gaplessgrid

### Keybindings

- `MOD+Shift+b`: Launch Chromium using spot(puppy linux).
- `MOD+Shift+n`: internet wizard for puppy linux.
- `MOD+q`: Open the power menu (shutdown, restart, etc.).
- `MOD+Shift+s`: Take a screenshot.
- `MOD+x`: Move mouse to (2000, 1200).
- `MOD+Shift+x`: Move mouse to (0, 1200).
- `F12`: Increase audio volume by 1%.
- `F11`: Decrease audio volume by 1%.
- `F10`: Toggle audio mute.
- `F5`: Decrease screen brightness by 1%.
- `F6`: Increase screen brightness by 1%.
- `F4`: Increase keyboard backlight by 10%.
- `F3`: Decrease keyboard backlight by 10%.
- `F7`: Run HDMI output script.
- `F8`: Run screen mirroring script.
- `F9`: Run split screen script.
- `Delete`: Close all dunst notifications.
- `MOD+d`: dmenu.
- `MOD+Shift+Return`: Open`st` with `zsh`.
- `MOD+b`: Toggle bar visibility.
- `MOD+j`: Focus next window.
- `MOD+k`: Focus previous window.
- `MOD+v`: Increase master window count.
- `MOD+Shift+d`: Decrease master window count.
- `MOD+h`: Decrease master area size.
- `MOD+l`: Increase master area size.
- `MOD+Return`: Zoom into the focused window.
- `MOD+Tab`: Switch between the last two windows.
- `MOD+c`: Close the focused window.
- `MOD+t`: Switch to tiled layout.
- `MOD+space`: Switch to floating layout.
- `MOD+m`: Switch to monocle layout.
- `MOD+g`: Switch to gapless grid layout.
- `MOD+f`: Toggle fullscreen mode.
- `MOD+Arrow keys`: Resize/move window (up/down/left/right).
- `MOD+Shift+Arrow keys`: Resize window (height/width).
- `MOD+Control+Arrow keys`: Resize window to screen edges.
- `MOD+0`: View all tags.
- `MOD+Shift+0`: Tag all windows.
- `MOD+comma/period`: Switch between monitors.
- `MOD+Shift+comma/period`: Move window between monitors.
- `MOD+s`: Toggle the first scratchpad (`spterm`).
- `MOD+r`: Toggle the second scratchpad (`spranger`).
- `MOD+1 to MOD+9`: Switch to corresponding tag.
- `MOD+Shift+1 to MOD+Shift+9`: Move window to corresponding tag.
- `MOD+Shift+q`: Quit DWM.

