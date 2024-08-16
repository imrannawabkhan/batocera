# batocera
Batocera Setup

# SSH Batocera By IP
User: root\
Password: linux

# Disk Space
```bash
$ df -h
```

# Virtualize
[Browse] https://www.inspekt.dev/2021/04/13/how-to-resize-virtualbox-hard-disk-vdi-file-virtualbox-resize-hard-disk-error-vbox_e_not_supported/

```bash 
$ "C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" convertdd D:\vms\batocera-x86_64-30-20210302.img D:\vms\Batocera\batocera-x86_64-30-20210302.vdi
```

-- 60 GB = 60000\
```bash 
$ "C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" modifyhd "D:\vms\Batocera\batocera-x86_64-30-20210302.vdi" --resize 60000
```

-- In case you want to increase the Storage Size\
```bash
$ cd C:\Program Files\Oracle\VirtualBox\ 
$ VBoxManage showhdinfo "D:\vms\Batocera\batocera-x86_64-30-20210302.vdi"
```

-- If Format Variant: fixed default
```bash
$ cd C:\Program Files\Oracle\VirtualBox\ 
$ VBoxManage clonehd "D:\vms\Batocera\batocera-x86_64-30-20210302.vdi" "D:\vms\Batocera\batocera-x86_64-30-20210302_updated.vdi"
```

# Expend Diskspace 
-- In case size increase by GUI
```bash
$ mount -o remount,rw /boot
$ cd /boot/
$ nano batocera-boot.conf
```

Uncomment the line #autoresize=true and save the file.
```bash
$ reboot -n
```

# WII Key Setup
[Browse] https://wiki.batocera.org/systems:wiiu

# Retrobat - How to remove multiple roms
[Browse] https://www.youtube.com/watch?v=YyaRwsd77EE

# How to convert a 118GB MAME ROM set down to 11.4GB removing clones, duplicates and unplayable games.
[Browse] https://www.youtube.com/watch?v=GZfoOTckURA

# Batocera Gamecube/Dolphin Emulation Setup Guide
[Browse] https://www.youtube.com/watch?v=J9OpYI3Z4Qc

# PSX BIOS
[Browse] https://www.retrostic.com/bios/pcsx-playstation

# PS3 BIOS
[Browse] https://androstalker.com/ps3-bios-download-files-emulator-free/

# How to Clone Your Batocera System
[Browse] https://www.youtube.com/watch?v=KaudH-Qu7UY\
[Software] AOMEI Partition Assistant 10.4.1

# Download Screenshots/Media for ROMS
-- Get ScreenScraper Account\
[Browse] https://www.screenscraper.fr/

-- Download and Install
[Software] https://www.skraper.net/

01- Login using screenscraper.fr credential\
02- Press [VALIDATE]\
03- Press [Next]\
04- [SELECT] RECALBOX 
05- Press [Next]\
06- Enter batocera's IP \\IPADDRESS\share\roms\
07- [Checked] Include non-Recalbox rom folders\
08- Press [Enter] to SCAN\
09- Press [Next] to finish\
10- [SELECT] the ROM on LEFT MENU\
11- [TAB] Media\
12- [Checked] Use specfic configuration for 3DO\
13- [Select] Media Type: Image and  Title Screen\
14- [Press] the Play Button at the bottom to continue.

# Wii controller setup
[Browse] https://www.reddit.com/r/batocera/comments/17velcs/custom_pad_profile_dolphin_workaround/

# Short Cuts
F2 - show time for 5 seconds (main Batocera menu and in game)\
F3 - enable/disable screen reader\
F4 - reboot Batocera\
F5 - updates it\
SPACE - shows BATOCERA's main menu\
ENTER - select itens\
ESC - goes back\
BACKSPACE on Home Screen - Fast menu options like next track sound or restart system or shutdown or airplain mode\
BACKSPACE on Console List Games - Search a game, select a random game, order by, and more!\
