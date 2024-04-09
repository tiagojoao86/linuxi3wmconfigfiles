# Arquivos de configuração do i3wm no Debian

- Debian Minimal Installation
- apt install i3 i3blocks
- apt install xorg
- apt install lightdm
- shutdown -r now
- apt install nitrogen mirage mc pulsemixer fonts-noto-color-emoji bluetooth blueman bluez tilix lxappearance net-tools inetutils-ping git
- copy config files in the project to SO
    - /etc/lightdm/lightdm-gtk-greeter.conf
    - /home/tiago/.bashrc
    - /home/tiago/.config/i3/config
    - /home/tiago/.config/i3blocks/config
    - /home/tiago/.config/picom.conf
    - /usr/share/lightdm/lightdm-gtk-greeter.conf.d/01_debian.conf
    - /usr/share/lightdm/lightdm.conf.d/01_my.conf
- Execute lxappearance, change to Adwaita-Dark
- apt install picom
- add to /etc/profile - export XDG_CONFIG_HOME="$HOME/.config"
- create symbol links to desire programs in a folder, e add that folder to $PATH in ~/.xsessionrc
