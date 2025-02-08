```bash
git clone https://github.com/markop404/dotfiles
cp -r ./dotfiles/home/* ~/
```
# Enable networking
```bash
sudo systemctl enable --now NetworkManager
```
# Install basic command-line utilities
```bash
sudo pacman -S curl git starship btop android-tools yazi man-db
```
# Install flatpak & xdg frameworks
```bash
sudo pacman -S flatpak xdg-desktop-portal xdg-desktop-portal-gtk xdg-desktop-portal-wlr xdg-user-dirs gnome-keyring
```
# Install distrobox
```bash
sudo pacman -S distrobox podman
```
# Install virt-manager
```bash
sudo pacman -S virt-manager qemu-base qemu-desktop
sudo systemctl enable libvirtd
sudo usermod -aG libvirt $(whoami)
```
# Install fonts & icon packs
```bash
sudo pacman -S papirus-icon-theme ttf-nerd-fonts-symbols ttc-iosevka
```
# Install my custom DE
```bash
sudo pacman -S sway swayidle waybar fuzzel foot
```
# Install power management
```bash
sudo pacman -S tuned
sudo systemctl enable tuned
```
# Install sound
```bash
sudo pacman -S pipewire pipewire-pulse wireplumber
systemctl enable --user pipewire-pulse.service
```
# Install brightness control
```bash
sudo pacman -S brightnessctl
```
# Install zram
```bash
sudo pacman -S zram-generator
```
# Set icon & dark theme globally
```bash
sudo pacman -S dconf
dconf write /org/gnome/desktop/interface/color-scheme "'prefer-dark'"
dconf write /org/gnome/desktop/interface/icon-theme "'Papirus-Dark'"
```