sudo pacman -S lxappearance wofi code qt5ct arc-solid-gtk-theme pamixer qt5-wayland brightnessctl nerd-fonts nautilus waybar obs-studio git bluez bluez-utils blueman viewnior vlc unzip grim slurp

links:
Waybar = https://github.com/catppuccin/waybar/tree/main
GRUB = https://github.com/catppuccin/grub
SDDM = https://github.com/catppuccin/sddm
Screenshot = https://github.com/emersion/grim

Create a file named "screenshot.sh" in path "/bin", then copy the code and paste it into the file:

-------------------------------------------------
#!/bin/bash

# Directory to save screenshots
SAVE_DIR="$HOME/Pictures/Screenshots"
mkdir -p "$SAVE_DIR"

# Timestamp for filename
TIMESTAMP=$(date +"%Y-%m-%d_%H-%M-%S")

# Screenshot file path
FILE="$SAVE_DIR/screenshot_$TIMESTAMP.png"

# Take screenshot
grim -g "$(slurp)" "$FILE"

# Notify user
notify-send "Screenshot saved to $FILE"

and execute this command line
sudo chmod +x ~/bin/screenshot.sh
-------------------------------------------------
Commands
sudo unzip catppuccin-mocha.zip -d /usr/share/sddm/themes
