# Instructions:
## Assumptions about your Mac

Your Mac must be fairly recent, with a core-i3/i5/i7 processor (64-bit EFI only). Hackintosh, Filevault, and Bootcamp are not officially supported - though Filevault and Bootcamp will work with additional setup.

## Installation:

1. Back everything up. No, really. Back. Everything. Up. This has been tested multiple times but anywhere there's code, there could be bugs.
2. [Download](http://cl.ly/380C3v3X0m1I/download/Elementary%20OS%20Install%20utility.app.zip) the app and open it

3. Click “Full install” and click "OK" to get started, then enter an admin name and password
4. Choose how much space to give Elementary OS in GB (Gigabytes) - slightly more than this much will be lost from your Mac and given to Elementary OS
5. Wait; this could take a while, do not stop or restart until the operation is complete.
6. Choose an ISO file downloaded from the [Elementary OS website](http://elementaryos.org) - the version must be at least Freya (0.3) which, as of this writing, is in beta
7. Click "OK" and restart your computer - you'll see the boot picker on startup
8. Press "ESC" and use the arrow keys to select the icon with the label "Boot EFI\BOOT\grubx64.efi" then select "Try Elementary OS without installing" and press enter
9. Click "Applications" in the top left and type "Terminal" then press enter. Type "`$ ubiquity -b`" into the Terminal and press enter (the dollar sign should not be typed; it just means it's for entering into a Terminal)
10. Click "Continue" then check "Install this third-party software." This will include closed-source software to allow you to play media files. You do not need to connect to a network.
11. Continue again and choose the disk you created earlier. It will be formatted fat32 with very little space used; it's probably at /dev/sda3 or /dev/sda4
12. Click "Change" in the bottom left and select "Use as: Ext4 journaling filesystem," check "Format the partition" and set the mount point to "/" then click "OK" and "Continue" if prompted
13. Click "Install now," ignoring any warnings about swap space, and select your time zone and keyboard layout (which should be auto-detected)
14. Fill out the prompts for name, username, password, etc. then continue
15. After installation is complete, click "Restart now"
16. Pray
17. When you see the boot picker, choose the icon that looks like an Elementary OS logo or a penguin
18. Have fun!
19. Boot into OS X and launch Elementary OS Install Utility again. Click "Erase installer" and enter your password - this will erase the installer so it never shows up again

## Troubleshooting
- If you're unsure if your Mac has 64-bit EFI, type `$ ioreg -l -p IODeviceTree | grep firmware-abi` into the OS X Terminal - if it spits out something along the lines of `firmware-abi" = <"EFI64">` then your EFI is 64-bit!
- If the boot picker stops showing up (e.g. after updating), launch the app again and click "Install Boot picker" - it should fix this
- If your computer fails to restart from Elementary OS, hold down the power button for five seconds to force a shutdown - this is a known bug with a fix being worked on
- If you run into any other issues, please report them! Email samuel@daitzman.com or go to http://github.com/sdaitzman/elementary-os-install-utility and click issues on the right hand side


This file references Install Elementary OS Utility version 6.0.2