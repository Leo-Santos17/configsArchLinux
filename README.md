# Initial Package
```
sudo pacman -S lxappearance wofi code qt5ct arc-solid-gtk-theme pamixer qt5-wayland brightnessctl nerd-fonts nautilus waybar obs-studio git bluez bluez-utils blueman viewnior vlc unzip grim slurp
```

## Links:
[Waybar (Catppuccin)](https://github.com/catppuccin/waybar/tree/main)

[GRUB (Catppuccin)](https://github.com/catppuccin/grub)

[SDDM (Catppuccin)](https://github.com/catppuccin/sddm)

[Screenshot (Catpuccin)](https://github.com/emersion/grim)


# Configuring
## Internet
```sh
nmcli device wifi list
nmcli device wifi connect _SSID_ password _password_
```
Verify this repository and proceed to hyprland.conf

## Hyprland
```
sudo nano ~/.config/hypr/hyprland.conf
```
## GRUB
```
sudo nano /etc/default/grub
```
Remove the # from the last line:
```
"GRUB_DISABLE_OS_PROBER=false"
```
Then access to GRUB link for insert a theme [GRUB](https://github.com/catppuccin/grub).

After, execute this commands
```
sudo os-prober
sudo grub-mkconfig -o /boot/grub/grub.cfg
```
## SDDM
Download the SDDM theme from the provided link and unzip it:
```
sudo unzip PATHtheme.zip /usr/share/sddm/themes/
```
## Waybar
View the guide at the provided Waybar link. To use my "waybar" configuration, copy the file into the "config" directory and follow the guide.

Restart the arch to verify the system


## Screenshot

Create a file named "screenshot.sh" in path "/bin", then copy the code and paste it into the file:
```
#!/bin/bash

# Directory to save screenshots
SAVE_DIR="$HOME/Pictures/Screenshots"
mkdir -p "$SAVE_DIR"View the guide at the provided Waybar link. To use my "waybar" configuration, copy the file into the "config" directory and follow the guide.

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
```
-------------------------------------------------

# Commands
```bash
sudo unzip catppuccin-mocha.zip -d /usr/share/sddm/themes
```
