<!-- TITLE: ERR-SYS-00001: Disappearing Windows with KDE/Plasma Desktop using Intel DDX -->
<!-- SUBTITLE: Intel X11/XFree86 Driver Issue and an Workaround -->

Summary
===========

When using Plasma 5.11.5 and KDE Frameworks 5.41.0 (and earlier) with a Intel X11/XFree86 driver (`xf86-video-intel`), some windows - specifically, those utillising GNOME/GTK+ 3 Client Side Decoration (or VTE 2.90?) - could fail to display on the screen. A taskbar entry of the window could be found, and a window preview should also display correctly. The window is not displaying, neither does it respond to any window management event: no cursor change when moving to the edge of the offending windows. Here are two instances of the issue:

- Tilix
- GNOME Terminal

Possible Cause
===========

Not yet identified.

Fixed Version
===========

None. However, a workaround has been identified - and this issue should only happen on a computer using Intel graphics (GMA, HD, UHD, etc.). To workaround this issue, you should switch to the "Modesetting" X11/XFree86 driver. To switch to this driver, simply add and apply the following configuration file with the instructions below:

Create a Custom X11 Configuration
------------------------------

Using your favourite editor (assuming `nano` here), create a custom X11 configuration file:

`sudo nano /etc/X11/xorg.conf.d/20-modesettings.conf`

Input in the following content:

```
Section "Device"
    Identifier  "Intel Graphics"
    Driver      "modesetting"
    Option      "AccelMethod"    "glamor"
    Option      "DRI"            "3"
EndSection
```

And finally, `Ctrl-X` then `Y` to save the file.

Restart Your X11 Session
---------------------

Using the following command:

`sudo systemctl restart display-manager`.

And you should be switched to the "Modesetting" driver, and that windows should be displaying correctly.