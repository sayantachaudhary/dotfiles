sudo pacman -S --noconfirm linux-lts linux-lts-headers
sudo pacman -S --noconfirm nvidia-open-dkms nvidia-utils nvidia-settings libva-nvidia-driver
echo "options nvidia_drm modeset=1" | sudo tee /etc/modprobe.d/nvidia.conf
sudo mkinitcpio -P
sudo grub-mkconfig -o /boot/grub/grub.cfg

https://wiki.hypr.land/Nvidia/
https://youtu.be/Pn2iUgW3l6w?si=-O52reqVLFTnNws9
Fix Screen Tearing in X11
