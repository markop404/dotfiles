```bash
git clone https://github.com/markop404/dotfiles
cp -r ./dotfiles/home/* ~/
```
# 0. Enable networking
```bash
sudo systemctl enable --now NetworkManager
```
# 1. Install basic utilities
```bash
sudo pacman -S curl git starship btop android-tools
```
# 2. Install flatpak & xdg frameworks
```bash
sudo pacman -S flatpak xdg-desktop-portal xdg-desktop-portal-gtk xdg-desktop-portal-wlr xdg-user-dirs gnome-keyring
```
# 3. Install distrobox
```bash
sudo pacman -S distrobox podman
```
# 4. Install virt-manager
```bash
sudo pacman -S virt-manager qemu-base qemu-desktop
sudo systemctl enable libvirtd
sudo usermod -aG libvirt $(whoami)
```
# 5. Install fonts & icon packs
```bash
sudo pacman -S ttf-nerd-fonts-symbols inter-font papirus-icon-theme
```
# 6. Install my custom DE
```bash
sudo pacman -S sway swayidle waybar fuzzel foot
```
# 7. Install thunar
```bash
sudo pacman -S thunar gvfs gvfs-mtp gvfs-smb
```
# 8. Install power management
```bash
sudo pacman -S tuned
```
# 9. Install sound
```bash
sudo pacman -S pipewire pipewire-pulse wireplumber
systemctl enable --user pipewire-pulse.service
```
# 10. Install brightness control
```bash
sudo pacman -S brightnessctl
```
# 11. Install zram
```bash
sudo pacman -S zram-generator
```
# 12. Set icon & dark theme globally
```bash
sudo pacman -S dconf
dconf write /org/gnome/desktop/interface/color-scheme "'prefer-dark'"
dconf write /org/gnome/desktop/interface/icon-theme "'Papirus-Dark'"
```
# 13. Install firmware updater
```bash
sudo pacman -S fwupd
```
