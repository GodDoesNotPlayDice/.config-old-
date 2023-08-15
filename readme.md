## How to Install

hello, everybody theses are my packages + dot files of garuda hyprland. 

you need to install garuda hyprland iso.
https://iso.builds.garudalinux.org/iso/community/hyprland/

### You have to follow this commands.

``` bash
# Install packages with pacman
# Firefox: Web browser
# Octopi: Graphical interface for managing Arch Linux packages
# Neofetch: Displays system information on the command line
# Discord: Chat and voice application for gamers
sudo pacman -S firefox octopi neofetch discord

# Uninstall firedragon
sudo pacman -R firedragon

# Install packages with pacman
# Squashfs-tools: Tools for working with SquashFS file systems
sudo pacman -S squashfs-tools


# Install packages with yay
# ttf-jetbrains-mono-nerd: JetBrains' monospaced font
# dracula-gtk-theme-git: Dracula theme for GTK
# dracula-icons-git: Dracula icons
# swappy: Wallpaper changer
yay -S ttf-jetbrains-mono-nerd dracula-gtk-theme-git dracula-icons-git swappy

# Copy and replace files in .config
cd ~/Downloads/
sudo git clone https://github.com/GodDoesNotPlayDice/.config ~/
cp -r ~/Downloads/.config/* ~/.config/


```


### After you can install some apps from snap
use the next bash
```bash
# Clone snapd from AUR and compile
# Snapd: Universal package manager for Linux distributions
git clone https://aur.archlinux.org/snapd.git
cd snapd
sudo chown -R user:user snapd/ # Rember change you user.
makepkg -si

# Enable and configure snapd
sudo systemctl enable --now snapd.socket
sudo ln -s /var/lib/snapd/snap /snap

# Install snap applications
# Code: Microsoft's source code editor
# GitKraken: Graphical interface for Git
# Postman: Platform for testing and developing APIs

sudo snap install code --classic
sudo snap install gitkraken --classic
sudo snap install postman

```

### Octopi install

Install additional applications
We use octopi instead of yay for the following applications
GitHub CLI: Command-line interface for GitHub GitHub Desktop: Graphical interface for GitHub
Ulauncher: Fast and lightweight application launcher
Google Chrome: Google's web browser


you have to install theses for Octopi

1) github-cli
2) github-desktop
3) ulauncher
4) google-chrome


### before execute you have to make chmod.
```bash
chmod +x script.sh
```


### Wallpapers 
https://github.com/whoisYoges/lwalpapers

config wallpapers in this file.

```bash
cd .config/wpaperd
kate .output.conf
```

```conf
[default]
path = "" # here add wallpaper's path
duration = "15m" # transition time
```


### SDDM (login screen)

i didn't inclue this in the dot files, you have to install this step to step.

1) choose a theme and download (.tar)
2) Extract in /Download
3) Copy and Paste theme in sddm/themes
```bash
sudo cp -r ~/Downloads/goodnight/ /usr/share/sddm/themes/goodnight/
```

4) Open sddm.conf
```bash 
kate /etc/sddm.conf
```

5) Edit current with the theme.
```conf
[Theme]
Current=goodnight
```

Source: https://github.com/Rokin05/SDDM-Themes

Dependences: 
```bash
pacman -S qt5-quickcontrols2 qt5-graphicaleffects qt5-svg
```
## Some images.

![Imagen](https://i.imgur.com/klwMWz9.png)

![Imagen](https://i.imgur.com/q4uFdpi.png)

![Imagen](https://i.imgur.com/HfwICyV.png)





