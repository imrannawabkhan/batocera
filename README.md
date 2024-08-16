# batocera
Batocera Setup

# SSH Batocera By IP
User: root
Password: linux

# Disk Space
df -h

# Virtualize
[Browser] https://www.inspekt.dev/2021/04/13/how-to-resize-virtualbox-hard-disk-vdi-file-virtualbox-resize-hard-disk-error-vbox_e_not_supported/

"C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" convertdd D:\vms\batocera-x86_64-30-20210302.img D:\vms\Batocera\batocera-x86_64-30-20210302.vdi

-- 60 GB = 60000
"C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" modifyhd "D:\vms\Batocera\batocera-x86_64-30-20210302.vdi" --resize 60000

-- In case you want to increase the Storage Size
cd C:\Program Files\Oracle\VirtualBox\ 
#VBoxManage showhdinfo "D:\vms\Batocera\batocera-x86_64-30-20210302.vdi"

-- If Format Variant: fixed default
#VBoxManage clonehd "D:\vms\Batocera\batocera-x86_64-30-20210302.vdi" "D:\vms\Batocera\batocera-x86_64-30-20210302_updated.vdi"

# Expend Diskspace 
-- In case size increase by GUI
#mount -o remount,rw /boot
cd /boot/
#nano batocera-boot.conf
Uncomment the line #autoresize=true
#reboot -n

[Save]
reboot -n

# WII Key Setup
https://wiki.batocera.org/systems:wiiu

# Retrobat - How to remove multiple roms
https://www.youtube.com/watch?v=YyaRwsd77EE

# How to convert a 118GB MAME ROM set down to 11.4GB removing clones, duplicates and unplayable games.
https://www.youtube.com/watch?v=GZfoOTckURA

# Batocera☆Gamecube/Dolphin Emulation Setup Guide
https://www.youtube.com/watch?v=J9OpYI3Z4Qc

# PSX BIOS
https://www.retrostic.com/bios/pcsx-playstation

# PS3 BIOS
https://androstalker.com/ps3-bios-download-files-emulator-free/

# How to Clone Your Batocera System
https://www.youtube.com/watch?v=KaudH-Qu7UY

# Wii controller setup
https://www.reddit.com/r/batocera/comments/17velcs/custom_pad_profile_dolphin_workaround/

# Short Cuts
F2 - show time for 5 seconds (main Batocera menu and in game)
F3 - enable/disable screen reader
F4 - reboot Batocera
F5 - updates it
SPACE - shows BATOCERA's main menu
ENTER - select itens
ESC - goes back
BACKSPACE on Home Screen - Fast menu options like next track sound or restart system or shutdown or airplain mode
BACKSPACE on Console List Games - Search a game, select a random game, order by, and more! 
