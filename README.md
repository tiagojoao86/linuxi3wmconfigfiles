# Debian 12

- Debian Minimal Installation
- apt install i3 i3blocks
- apt install xorg
- apt install lightdm
- shutdown -r now
- apt install nitrogen mirage mc pulseaudio pulsemixer fonts-noto-color-emoji bluetooth blueman bluez tilix lxappearance net-tools inetutils-ping git network-manager
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
- to add folders to path for dmenu, you should export $PATH in ~/.xsessionrc

# Rocky Linux 9

- Rocky Minimal Installation
- dnf config-manager --set-enabled crb
- dnf config-manager --set-enabled extras
- dnf install epel-release --assumeyes
- dnf install rpmfusion-free-release --assumeyes
- dnf install wget git --assumeyes
- wget $(echo "https://pkgs.dyn.su/el9/base/x86_64/raven-release.el9.noarch.rpm" | sed "s/el9/el$(rpm -q --queryformat '%{RELEASE}' rpm | grep -oP 'el\K[0-9]+')/g")
- sudo rpm -ivh raven-release*.rpm
- sudo dnf clean all && sudo dnf update --assumeyes
- dnf install i3 automake 
- dnf groupinstall "Development Tools"
- git clone https://github.com/vivien/i3blocks
    - cd i3blocks
    - ./autogen.sh
    - ./configure
    - make
    - make install
- dnf install xorg-x11-server-Xorg
- dnf install lightdm --assumeyes
- systemctl set-default graphical
- shutdown -r now
- In ~/.config/i3/config ajust the status_command to full path where's i3blocks command
- dnf install tilix mc lxappearance google-noto-emoji-color-fonts acpi sysstat lm_sensors neovim picom
- dnf install langpacks-pt
- localectl set-locale LANG=pt_BR.UTF8 (run with local user)
- add to /etc/profile - export XDG_CONFIG_HOME="$HOME/.config"
- i3blocks ajusts
    - ~/.config/i3blocks/config
        - In [MEM] change Mem.: to Mem:
