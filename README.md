<img width=150 height=50 align=left src="https://swaywm.org/logo.png">
<img width=150 height=50 align=right src="https://archlinux.org/static/logos/archlinux-logo-light-1200dpi.7ccd81fd52dc.png">

<br><br>

<h1 align="center">swayXde</h1>

<h6 align="right"><em>My attempt to create a desktop environment for Sway</em></h1>


## Installation

There is no installation script yet, but in the meantime you can clone the repo and copy the contents of the `./config` folder into your `./config` folder.

<u>Example</u>:

```
git clone https://github.com/p2ndemic/dotfiles.git
cp -r dotfiles/.config/* ~/.config
```

### TODO

- [ ] Add installation script
- [ ] Better documentation

## Screenshots


## 🖥️ OS & Core Components

| Module Type | Module Name | Optional | Note |
|-------------|-------------|----------|------|
| 💻 OS                 | [Arch Linux](https://archlinux.org/) | [CachyOS](https://cachyos.org/) |
| 🐧 Kernel             | [linux-prjc-lfbmq](https://gitlab.com/alfredchen/linux-prjc/-/tree/linux-6.17.y-prjc-lfbmq) | | _[Benchmark](https://www.reddit.com/r/linux_gaming/comments/1nkg0lr/update_on_my_bmq_scheduler_post_a_sidebyside/)_ |
| 🗃️ File System        | [efitools](https://archlinux.org/packages/extra/x86_64/efitools/) · [smartmontools](https://archlinux.org/packages/extra/x86_64/smartmontools/) · [xfsprogs](https://archlinux.org/packages/core/x86_64/xfsprogs/) | [nfs-utils](https://wiki.archlinux.org/title/NFS) · [nilfs-utils](https://wiki.archlinux.org/title/NILFS2) · [fsarchiver](https://archlinux.org/packages/extra/x86_64/fsarchiver/)| _[Arch Wiki](https://wiki.archlinux.org/title/File_systems)_ ➟ _[xfs_config](https://github.com/p2ndemic/dotfiles/blob/main/etc/sysctl.d/99-xfs-sync-interval.conf)_ ➟ _sudo systemctl enable --now fstrim.timer_ ➟ _sudo systemctl enable --now xfs_scrub_all.timer_ |
| 🔧 Hardware Utils     | [dmidecode](https://archlinux.org/packages/extra/x86_64/dmidecode/) · [hwdetect](https://wiki.archlinux.org/title/Hwdetect) · [hdparm](https://archlinux.org/packages/core/x86_64/hdparm/) · [usbutils](https://archlinux.org/packages/core/x86_64/usbutils/) | [hwinfo](https://archlinux.org/packages/extra/x86_64/hwinfo/) · [dmraid](https://archlinux.org/packages/core/x86_64/dmraid/) |
| 🕒 NTP Daemon         | [systemd-timesyncd](https://www.freedesktop.org/software/systemd/man/latest/systemd-timesyncd.service.html) | [chrony](https://wiki.archlinux.org/title/Chrony) | _[Arch Wiki](https://wiki.archlinux.org/title/Systemd-timesyncd)_ ➟ _[timesyncd_config](https://github.com/p2ndemic/dotfiles/blob/main/etc/systemd/timesyncd.conf.d/99-local.conf)_ ➟ _sudo systemctl enable --now systemd-timesyncd.service_ |
| ⚡ Power Management   | [upower](https://archlinux.org/packages/extra/x86_64/upower/) · [poweralertd](https://sr.ht/~kennylevinsen/poweralertd/) · [tuned](https://wiki.archlinux.org/title/CPU_frequency_scaling#tuned) ﹢ [tuned-gui](https://wiki.archlinux.org/title/CPU_frequency_scaling#tuned) | [tuned-ppd](https://archlinux.org/packages/extra/any/tuned-ppd/) · [systemtap](https://archlinux.org/packages/extra/x86_64/systemtap/) · [wireless_tools](https://archlinux.org/packages/extra/x86_64/wireless_tools/) · [laptop-mode-tools](https://wiki.archlinux.org/title/Laptop_Mode_Tools) | _[Arch Wiki](https://wiki.archlinux.org/title/Power_management)_ ➟ _[tuned Wiki](https://wiki.archlinux.org/title/TuneD)_ ➟ _sudo systemctl enable --now tuned.service_ ➟ _systemctl --user enable --now poweralertd.service_|
| 📦 Package Management | [pacman-contrib](https://archlinux.org/packages/extra/x86_64/pacman-contrib/) · [plocate](https://wiki.archlinux.org/title/Locate) · [pkgfile](https://wiki.archlinux.org/title/Pkgfile) · [reflector](https://wiki.archlinux.org/title/Reflector) · [rebuild-detector](https://archlinux.org/packages/extra/any/rebuild-detector/) · [git](https://wiki.archlinux.org/title/Git) · [octopi](https://aur.archlinux.org/packages/octopi) | | _[Arch Wiki](https://wiki.archlinux.org/title/Pacman)_ |
| 🧊 Archiving & Compression | [zlib-ng](https://archlinux.org/packages/extra/x86_64/zlib-ng/) · [zlib-ng-compat](https://archlinux.org/packages/extra/x86_64/zlib-ng-compat/) · [libarchive](https://archlinux.org/packages/core/x86_64/libarchive/) · [7zip](https://archlinux.org/packages/extra/x86_64/7zip/) · [arqiver](https://aur.archlinux.org/packages/arqiver) |
| 🅰️ Font rendering     | [freetype2](https://archlinux.org/packages/extra/x86_64/freetype2/) · [fontconfig](https://archlinux.org/packages/extra/x86_64/fontconfig/) |
| 🧙 AUR Helpers        | [chaotic-aur](https://aur.chaotic.cx/) · [yay](https://aur.archlinux.org/packages/yay) | [paru](https://aur.archlinux.org/packages/paru) | 💀 _[Сhaotic Wiki](https://aur.chaotic.cx/docs)_ |

---

## 🧬 Drivers & Firmware

| Module Type | Module Name | Optional | Note |
|-------------|-------------|----------|------|
| ⚙️ Linux Firmware | [linux-firmware](https://archlinux.org/packages/core/any/linux-firmware/) · [sof-firmware](https://archlinux.org/packages/extra/x86_64/sof-firmware/) | [fwupd](https://archlinux.org/packages/extra/x86_64/fwupd/) | _[Arch Wiki](https://wiki.archlinux.org/title/Linux_firmware)_ · _[SOF Doc](https://thesofproject.github.io/latest/getting_started/intel_debug/introduction.html)_ · _[fwupd Wiki](https://wiki.archlinux.org/title/Fwupd)_ |

### 🔹 Intel Drivers

| Module Type | Module Name | Optional | Note |
|-------------|----------|----------|------|
| 🔹 Intel Microcode      | [intel-ucode](https://archlinux.org/packages/extra/any/intel-ucode/) |
| 🔹 Intel Vulkan         | [mesa](https://archlinux.org/packages/extra/x86_64/mesa/) · [vulkan-intel](https://archlinux.org/packages/extra/x86_64/vulkan-intel) · [vulkan-icd-loader](https://archlinux.org/packages/extra/x86_64/vulkan-icd-loader/) · [vulkan-headers](https://archlinux.org/packages/extra/any/vulkan-headers/) · [vulkan-mesa-layers](https://archlinux.org/packages/extra/x86_64/vulkan-mesa-layers/) · [vulkan-tools](https://archlinux.org/packages/extra/x86_64/vulkan-tools/) · [mesa-utils](https://archlinux.org/packages/extra/x86_64/mesa-utils/) | [vulkan-validation-layers](https://archlinux.org/packages/extra/x86_64/vulkan-validation-layers/) · [vulkan-extra-layers](https://archlinux.org/packages/extra/x86_64/vulkan-extra-layers/) | _[Arch Wiki](https://wiki.archlinux.org/title/Vulkan)_ · _[Mesa Doc](https://docs.mesa3d.org/envvars.html)_ |
| 🔹 Intel OpenCL         | [intel-compute-runtime](https://archlinux.org/packages/extra/x86_64/intel-compute-runtime/) · [opencl-headers](https://archlinux.org/packages/extra/any/opencl-headers/) · [ocl-icd](https://archlinux.org/packages/extra/x86_64/ocl-icd/) | [opencl-icd-loader](https://aur.archlinux.org/packages/opencl-icd-loader)  | _[Arch Wiki](https://wiki.archlinux.org/title/GPGPU)_ ➟ _env OCL_ICD_VENDORS=/etc/OpenCL/vendors/intel.icd_ |
| 🔹 Intel VA-API         | [intel-media-driver](https://archlinux.org/packages/extra/x86_64/intel-media-driver/) · [vpl-gpu-rt](https://archlinux.org/packages/extra/x86_64/vpl-gpu-rt/) · [libvpl-tools](https://archlinux.org/packages/extra/x86_64/libvpl-tools/) | | _[Arch Wiki](https://wiki.archlinux.org/title/Hardware_video_acceleration)_ ➟ _env LIBVA_DRIVER_NAME=iHD_ |
| 🌡️ Intel Thermal Daemon | [thermald](https://archlinux.org/packages/extra/x86_64/thermald/) | | _[Arch Wiki](https://wiki.archlinux.org/title/CPU_frequency_scaling#thermald)_ ➟ _sudo systemctl enable --now thermald_ |
| 1️⃣ oneAPI               | [level-zero-loader](https://archlinux.org/packages/extra/x86_64/level-zero-loader/) · [level-zero-headers](https://archlinux.org/packages/extra/x86_64/level-zero-headers/) |
| 🧪 Intel GPU Tools      | _optional_ | [intel-gpu-tools](https://archlinux.org/packages/extra/x86_64/intel-gpu-tools/) |
| 🔧 adriconf             | _optional_ | [adriconf](https://archlinux.org/packages/extra/x86_64/adriconf/) | 

---

### 🔸 AMD Drivers

| Module Type | Module Name | Optional | Note |
|-------------|-------------|----------|------|
| 🔸 AMD Microcode | [amd-ucode](https://archlinux.org/packages/core/any/amd-ucode) | |  _[Arch Wiki](https://wiki.archlinux.org/title/Microcode)_ |
| 🔸 AMD Vulkan    | [mesa](https://archlinux.org/packages/extra/x86_64/mesa/) · [vulkan-radeon](https://archlinux.org/packages/extra/x86_64/vulkan-radeon/) · [vulkan-icd-loader](https://archlinux.org/packages/extra/x86_64/vulkan-icd-loader/) · [vulkan-headers](https://archlinux.org/packages/extra/any/vulkan-headers/) · [vulkan-mesa-layers](https://archlinux.org/packages/extra/x86_64/vulkan-mesa-layers/) · [vulkan-tools](https://archlinux.org/packages/extra/x86_64/vulkan-tools/) · [mesa-utils](https://archlinux.org/packages/extra/x86_64/mesa-utils/) | [vulkan-validation-layers](https://archlinux.org/packages/extra/x86_64/vulkan-validation-layers/) · [vulkan-extra-layers](https://archlinux.org/packages/extra/x86_64/vulkan-extra-layers/) | _[Arch Wiki](https://wiki.archlinux.org/title/Vulkan)_ · _[Mesa Doc](https://docs.mesa3d.org/envvars.html)_ |
| 🔸 AMD OpenCL    | [opencl-mesa](https://archlinux.org/packages/extra/x86_64/opencl-mesa/) · [opencl-headers](https://archlinux.org/packages/extra/any/opencl-headers/) · [ocl-icd](https://archlinux.org/packages/extra/x86_64/ocl-icd/)  | [rocm-opencl-runtime](https://archlinux.org/packages/extra/x86_64/rocm-opencl-runtime/) · [opencl-icd-loader](https://aur.archlinux.org/packages/opencl-icd-loader) | _[Arch Wiki](https://wiki.archlinux.org/title/GPGPU)_ ➟ _env RUSTICL_ENABLE=radeonsi_ |
| 🔸 AMD VA-API    | [mesa](https://archlinux.org/packages/extra/x86_64/mesa/) | | _[Arch Wiki](https://wiki.archlinux.org/title/Hardware_video_acceleration)_ ➟ _env LIBVA_DRIVER_NAME=radeonsi_ |
| 🔧 adriconf               | _optional_ | [adriconf](https://archlinux.org/packages/extra/x86_64/adriconf/) | 

---

### 🌐 Network Drivers & Utils
| Module Type | Module Name | Optional | Note |
|-------------|-------------|----------|------|
| 🔹 Network Drivers & Utils   | [ethtool](https://archlinux.org/packages/extra/x86_64/ethtool/) · [iwd](https://archlinux.org/packages/extra/x86_64/iwd/) · [wireless-regdb](https://archlinux.org/packages/core/any/wireless-regdb/) · _[xl2tpd](https://archlinux.org/packages/extra/x86_64/xl2tpd/)_ | _[nss-mdns](https://archlinux.org/packages/extra/x86_64/nss-mdns/)_ | _[iwd_config](https://github.com/p2ndemic/dotfiles/blob/main/etc/iwd/main.conf)_ ➟ _[wireless-regdom_config](https://github.com/p2ndemic/dotfiles/blob/main/etc/conf.d/wireless-regdom)_ ➟ _rfkill unblock wlan_ |
| 🔹 Network Management Service   | [systemd-networkd](https://wiki.archlinux.org/title/Systemd-networkd) | [networkmanager](https://wiki.archlinux.org/title/NetworkManager) · _[usb_modeswitch](https://archlinux.org/packages/extra/x86_64/usb_modeswitch/)_ · _[modemmanager](https://archlinux.org/packages/extra/x86_64/modemmanager/)_ · _[networkmanager_plugins](https://networkmanager.dev/docs/vpn/)_ |  _[Arch Wiki](https://wiki.archlinux.org/title/Systemd-networkd)_ ➟ **_[systemd-networkd_ethernet_config](https://github.com/p2ndemic/dotfiles/blob/main/etc/systemd/network/20-wired.network)_** ➟ **_[systemd-networkd_wlan_config](https://github.com/p2ndemic/dotfiles/blob/main/etc/systemd/network/25-wireless.network)_** ➟ **_sudo systemctl disable --now NetworkManager wpa_supplicant && sudo systemctl enable --now iwd systemd-networkd systemd-resolved_** ➟ **_sudo ln -sf /run/systemd/resolve/stub-resolv.conf /etc/resolv.conf_** · _Optional:_ _[nm_config](https://github.com/p2ndemic/dotfiles/blob/main/etc/NetworkManager/conf.d/99-iwd.conf)_ ➟  _[nm_dns_config](https://github.com/p2ndemic/dotfiles/blob/main/etc/NetworkManager/conf.d/99-dns.conf)_  ➟ _sudo systemctl enable --now NetworkManager.service_ |
| 🔹 DNS Resolver                 | [systemd-resolved](https://wiki.archlinux.org/title/Systemd-resolved) | [unbound](https://wiki.archlinux.org/title/Unbound) | _[Arch Wiki](https://wiki.archlinux.org/title/Domain_name_resolution)_ ➟ _[systemd-resolved_config](https://github.com/p2ndemic/dotfiles/blob/main/etc/systemd/resolved.conf.d/99-resolved.conf)_ ➟ _sudo systemctl enable --now systemd-resolved.service_ ➟ _**[disable Avahi]**_ ➟ _sudo systemctl disable --now avahi-daemon.service avahi-daemon.socket_ ➟ _sudo systemctl mask avahi-daemon.service avahi-daemon.socket_ |
| 🌍 _..._ _Connect to a Network_ | [iwd](https://archlinux.org/packages/extra/x86_64/iwd/) ﹢ [iwgtk](https://aur.archlinux.org/packages/iwgtk) | | _[iwd Wiki](https://wiki.archlinux.org/title/Iwd)_ ➟ _[iwd Man](https://man.archlinux.org/man/iwctl.1)_ ➟ _[iwd_config](https://github.com/p2ndemic/dotfiles/blob/main/etc/iwd/main.conf)_ ➟ _**Connect to a network**_ ➟ _**[Command line mode]**_ ➟ _iwctl --help_ ➟ _iwctl device list_ ➟ _iwctl station DEVICE scan_ ➟ _iwctl station DEVICE get-networks_ ➟ _iwctl --passphrase=PASSPHRASE station DEVICE connect SSID_ \| _**[Interactive mode]**_ ➟ _iwctl_ ➟ _help_ ➟ _..._|

---

### 🎧 Sound Drivers & Codecs
| Module Type | Module Name | Optional | Note |
|-------------|-------------|----------|------|
| 🎛️ ALSA                | [alsa-firmware](https://archlinux.org/packages/extra/any/alsa-firmware/) · [alsa-utils](https://archlinux.org/packages/extra/x86_64/alsa-utils/) · [alsa-plugins](https://archlinux.org/packages/extra/x86_64/alsa-plugins/) · [alsa-card-profiles](https://archlinux.org/packages/extra/x86_64/alsa-card-profiles/) | | _[Arch Wiki](https://wiki.archlinux.org/title/Advanced_Linux_Sound_Architecture)_ |
| 🔊 Piperwire           | [pipewire](https://archlinux.org/packages/extra/x86_64/pipewire/) · [pipewire-alsa](https://archlinux.org/packages/extra/x86_64/pipewire-alsa/) · [pipewire-pulse](https://archlinux.org/packages/extra/x86_64/pipewire-pulse/) · [pwvucontrol](https://github.com/saivert/pwvucontrol) | [pipewire-jack](https://archlinux.org/packages/extra/x86_64/pipewire-jack/) · [pipewire-libcamera](https://archlinux.org/packages/extra/x86_64/pipewire-libcamera/) · [pavucontrol](https://archlinux.org/packages/extra/x86_64/pavucontrol/)| _[Arch Wiki](https://wiki.archlinux.org/title/PipeWire)_ ➟ systemctl --user enable --now pipewire ➟ systemctl --user enable --now pipewire-pulse |
| 🪄 Wireplumber & Utils | [wireplumber](https://archlinux.org/packages/extra/x86_64/wireplumber/) · [rtkit](https://archlinux.org/packages/extra/x86_64/rtkit/) | | _[Arch Wiki](https://wiki.archlinux.org/title/WirePlumber)_ ➟ systemctl --user enable --now wireplumber ➟ sudo systemctl enable --now rtkit |
| 🌊 GStreamer           | [gst-libav](https://archlinux.org/packages/extra/x86_64/gst-libav/) · [gst-plugin-va](https://archlinux.org/packages/extra/x86_64/gst-plugin-va/) · [gst-plugins-base](https://archlinux.org/packages/extra/x86_64/gst-plugins-base/) · [gst-plugins-bad](https://archlinux.org/packages/extra/x86_64/gst-plugins-bad/) · [gst-plugins-good](https://archlinux.org/packages/extra/x86_64/gst-plugins-good/) · [gst-plugins-ugly](https://archlinux.org/packages/extra/x86_64/gst-plugins-ugly/) · [gst-plugin-pipewire](https://archlinux.org/packages/extra/x86_64/gst-plugin-pipewire/) | | _env GST_VA_ALL_DRIVERS=1_ |
| 📼 FFmpeg              | [ffmpeg](https://archlinux.org/packages/extra/x86_64/ffmpeg/) |
| 📑 Misc                | [ffmpegthumbnailer](https://archlinux.org/packages/extra/x86_64/ffmpegthumbnailer/) · [libdvdcss](https://archlinux.org/packages/extra/x86_64/libdvdcss/) · [libopenraw](https://archlinux.org/packages/extra/x86_64/libopenraw/) | 

### 🔹 Bluetooth Drivers & Utils
| Module Type | Module Name | Optional | Note |
|-------------|-------------|----------|------|
| 🔹 Bluetooth Drivers | [bluez](https://wiki.archlinux.org/title/Bluetooth) · [bluez-libs](https://archlinux.org/packages/extra/x86_64/bluez-libs/) · [bluez-utils](https://archlinux.org/packages/extra/x86_64/bluez-utils/) · [bluez-hid2hci](https://archlinux.org/packages/extra/x86_64/bluez-hid2hci/) | [bluez-obex](https://archlinux.org/packages/extra/x86_64/bluez-obex/) | _[Arch Wiki](https://wiki.archlinux.org/title/Bluetooth)_ ➟  _rfkill unblock bluetooth_ ➟ _sudo systemctl enable --now bluetooth.service_ |
| 🔹 Bluetooth Utils | [blueman](https://github.com/blueman-project/blueman) | [overskride](https://github.com/kaii-lb/overskride) |


---

## 🧩 Wayland Stack
| Module Type | Module Name  | Alternative |
|-------------|--------------|-------------|
| 🔰 Wayland Compositor      | [sway](https://github.com/swaywm/sway) \| [labwc](https://wiki.archlinux.org/title/Labwc) | [mango](https://wiki.archlinux.org/title/MangoWM) \| [niri](https://wiki.archlinux.org/title/Niri) |
| 📜 Wayland Protocols       | [wayland-protocols](https://gitlab.freedesktop.org/wayland/wayland-protocols) ﹢ [wlr-protocols](https://gitlab.freedesktop.org/wlroots/wlr-protocols) ﹢ [frog-protocols](https://github.com/misyltoad/frog-protocols) |
| 📗 Wayland Integration     | [egl-wayland](https://archlinux.org/packages/extra/x86_64/egl-wayland/) · [xorg-xwayland](https://archlinux.org/packages/extra/x86_64/xorg-xwayland/) · [qt5-wayland](https://archlinux.org/packages/extra/x86_64/qt5-wayland) · [qt6-wayland](https://archlinux.org/packages/extra/x86_64/qt6-wayland)
| 🧵 Wayland Session Manager | [uwsm ](https://wiki.archlinux.org/title/Universal_Wayland_Session_Manager) ﹢ [ [util-linux](https://archlinux.org/packages/core/x86_64/util-linux/) · [libnewt](https://archlinux.org/packages/extra/x86_64/libnewt/) · [inotify-tools](https://archlinux.org/packages/extra/x86_64/inotify-tools/) ]|
| 🔐 Authentication Agent    | [polkit](https://wiki.archlinux.org/title/Polkit) · [lxqt-policykit](https://archlinux.org/packages/extra/x86_64/lxqt-policykit/) |
| 🌀 XDG Portal Backend      | [xdg-desktop-portal](https://wiki.archlinux.org/title/XDG_Desktop_Portal) · [xdg-desktop-portal-wlr](https://archlinux.org/packages/extra/x86_64/xdg-desktop-portal-wlr/) · [xdg-desktop-portal-lxqt](https://archlinux.org/packages/extra/x86_64/xdg-desktop-portal-lxqt/)
| 🗂️ XDG User Dirs & Utils   | [xdg-user-dirs](https://wiki.archlinux.org/title/XDG_user_directories) · [xdg-utils](https://wiki.archlinux.org/title/Xdg-utils) |
| 👤 User Account Service    | [accountsservice](https://archlinux.org/packages/extra/x86_64/accountsservice/) |
| 🪟 Display Manager         | _none_ | [greetd](https://git.sr.ht/~kennylevinsen/greetd) ﹢ [regreet](https://github.com/rharish101/ReGreet) \| [ly](https://codeberg.org/fairyglade/ly) |

---

## 🐚 Terminal & Shell

| Module Type | Module Name | Alternative |
|-------------|-------------|-------------|
| 🐟 Shell             | [fish](https://github.com/fish-shell/fish-shell) |
| 💫 Shell Enhancers   | [fastfetch](https://github.com/fastfetch-cli/fastfetch) ﹢ [starship](https://github.com/starship/starship) ﹢ [navi](https://github.com/denisidoro/navi) ﹢ [bash-completion](https://archlinux.org/packages/extra/any/bash-completion/) |
| 📟 Terminal Emulator | [foot](https://codeberg.org/dnkl/foot) |
| 🚀 App Launcher      | [fuzzel](https://codeberg.org/dnkl/fuzzel) ﹢ [fuzzel-custom-menu](https://github.com/p2ndemic/dotfiles/blob/main/.local/bin/fuzzel-launcher-index.sh) ﹢ [fuzzel-powermenu](https://github.com/p2ndemic/dotfiles/blob/main/.local/bin/fuzzel-powermenu-index.sh) | [walker](https://github.com/abenz1267/walker) |

---

## 🔰 WC Core Modules
| Module Type | Module Name | Optional | Alternative |
|-------------|-------------|----------|-------------|
| 🖥️ Display Management | [wlr-randr](https://gitlab.freedesktop.org/emersion/wlr-randr) ﹢ [kanshi](https://sr.ht/~emersion/kanshi) | | [nwg-displays](https://github.com/nwg-piotr/nwg-displays) |
| 💾 Device & Volume Management | [udiskie](https://archlinux.org/packages/extra/any/udiskie/) | [pcmanfm-qt](https://github.com/lxqt/pcmanfm-qt) ﹢ [gvfs](https://wiki.archlinux.org/title/File_manager_functionality#Mounting) |
| 🖼️ Wallpaper Management       | [swaybg](https://github.com/swaywm/swaybg) | [pcmanfm-qt](https://github.com/lxqt/pcmanfm-qt) |
| 💤 Idle Management            | [swayidle](https://github.com/swaywm/swayidle) |
| 🔒 Screen Lock                | [swaylock](https://github.com/swaywm/swaylock) ﹢ [wlopm](https://archlinux.org/packages/extra/x86_64/wlopm/) | [chayang](https://aur.archlinux.org/packages/chayang) |
| 🔔 Notification Daemon        | [mako](https://github.com/emersion/mako) | | [fnott](https://codeberg.org/dnkl/fnott) |
| 📋 Clipboard Management       | [wl-clipboard-rs](https://github.com/YaLTeR/wl-clipboard-rs) ﹢ [wl-clip-persist](https://github.com/Linus789/wl-clip-persist) ﹢ [cliphist](https://github.com/sentriz/cliphist) | | [wl-clipboard](https://github.com/bugaevc/wl-clipboard) \| [clipse](https://github.com/savedra1/clipse) |
| ☄️ Status Bar                 | [waybar](https://github.com/Alexays/Waybar) | | [DankMaterialShell](https://github.com/AvengeMedia/DankMaterialShell) \| [ironbar](https://github.com/JakeStanger/ironbar)  \| [vibepanel](https://github.com/prankstr/vibepanel)|
| 🎴 OSD / Overlay              | [wob](https://github.com/francma/wob) ﹢ [wob-brightness.sh](https://github.com/p2ndemic/dotfiles/blob/main/.local/bin/wob-brightness.sh) ﹢ [wob-volume.sh](https://github.com/p2ndemic/dotfiles/blob/main/.local/bin/wob-volume.sh)
| 🔆 Brightness Control         | [brightnessctl](https://github.com/Hummer12007/brightnessctl) | [gammastep](https://gitlab.com/chinstrap/gammastep) \| [wlsunset](https://git.sr.ht/~kennylevinsen/wlsunset) \| [wluma](https://github.com/maximbaz/wluma) |

## 🔰 WC Specific Modules

### 🔹 Sway
| Module Type | Module Name | Unit |  Note |
|-------------|-------------|------|-------|
| 🔹 Display Management    | _sway internal_ |
| 🔹 Device Automount     | [udiskie](https://archlinux.org/packages/extra/any/udiskie/) | _[udiskie.service](https://github.com/p2ndemic/dotfiles/blob/main/.config/systemd/user/udiskie.service)_ | _[udisks Wiki](https://wiki.archlinux.org/title/Udisks)_ ⤍ _[udiskie Wiki](https://github.com/coldfix/udiskie/wiki/Usage)_ ⤍ _systemctl --user enable --now udiskie.service_
| 🔹 Wallpaper Management | [swaybg](https://github.com/swaywm/swaybg) | _[swaybg.service](https://github.com/p2ndemic/dotfiles/blob/main/.config/systemd/user/swaybg.service)_ | _systemctl --user enable --now swaybg.service_ |
| 🔹 Status Bar           | [waybar](https://wiki.archlinux.org/title/Waybar) | _[waybar.service](https://github.com/p2ndemic/dotfiles/blob/main/.config/systemd/user/waybar.service)_ | _[sway_waybar_config](https://github.com/p2ndemic/dotfiles/blob/main/.config/waybar/config.jsonc)_ ⤍ _systemctl --user enable --now waybar.service_
| 🔹 Autotiling           | [autotiling-rs](https://github.com/ammgws/autotiling-rs) | _[autotiling-rs.service](https://github.com/p2ndemic/dotfiles/blob/main/.config/systemd/user/autotiling-rs.service)_ | _systemctl --user enable --now autotiling-rs.service_
| 🔹 Window Switcher      | [wswitch](https://github.com/DreamMaoMao/wswitch) \| [snappy-switcher](https://github.com/OpalAayan/snappy-switcher) | _[]()_ | _systemctl --user enable --now .service_


### 🔸 Labwc
| Module Type | Module Name | Unit |  Note |
|-------------|-------------|------|-------|
| 🔸 Display Management      | [wlr-randr](https://gitlab.freedesktop.org/emersion/wlr-randr) ﹢ [kanshi](https://sr.ht/~emersion/kanshi) | _[kanshi.service](https://github.com/p2ndemic/dotfiles/blob/main/.config/systemd/user/kanshi.service)_ | _[kanshi_conig](https://github.com/p2ndemic/dotfiles/blob/main/.config/kanshi/config)_ ⤍ _systemctl --user enable --now kanshi.service_
| 🔸 Device Automount       | [pcmanfm-qt](https://github.com/lxqt/pcmanfm-qt) ﹢ [gvfs](https://wiki.archlinux.org/title/File_manager_functionality#Mounting) | _[pcmanfm-qt.service](https://github.com/p2ndemic/dotfiles/blob/main/.config/systemd/user/pcmanfm-qt.service)_ | _[gvfs Wiki](https://wiki.gnome.org/Projects/gvfs/doc)_ ➟ _[pcmanfm-qt Wiki](https://github.com/lxqt/pcmanfm-qt/wiki#gvfs)_ ⤍ _[pcmanfm-qt Daemon Mode Wiki](https://lxqt-project.org/wiki/Pcmanfm-qt.html#using-desktop-under-wayland)_ ⤍ _**env GVFS_DISABLE_FUSE=1**_ ⤍ _systemctl --user enable --now pcmanfm-qt.service_ |
| 🔸 Wallpaper Management   | [pcmanfm-qt](https://wiki.archlinux.org/title/PCManFM) | _[pcmanfm-qt.service](https://github.com/p2ndemic/dotfiles/blob/main/.config/systemd/user/pcmanfm-qt.service)_ | _systemctl --user enable --now pcmanfm-qt.service_
| 🔸 Status Bar             | [waybar](https://wiki.archlinux.org/title/Waybar) | _[waybar.service](https://github.com/p2ndemic/dotfiles/blob/main/.config/systemd/user/waybar.service)_ | _[labwc_waybar_config](https://github.com/p2ndemic/dotfiles/blob/main/.config/waybar/config.jsonc)_ ⤍ _systemctl --user enable --now waybar.service_
| 🔸 Keyboard state monitor | [xkb-monitor](https://github.com/drougas/xkb-monitor) | | _[waybar_config](https://github.com/p2ndemic/dotfiles/blob/main/.config/waybar/config.jsonc)_


---

## 📦 Applications

| Module Type | Module Name | Optional | Alternative |
|-------------|-------------|----------|-------------|
| 🔧 CLI      | [jq](https://jqlang.org/) · [bat](https://github.com/sharkdp/bat) · [eza](https://github.com/eza-community/eza) · [fzf](https://github.com/junegunn/fzf) · [inxi](https://codeberg.org/smxi/inxi) · [caligula](https://archlinux.org/packages/extra/x86_64/caligula/) · [duf](https://github.com/muesli/duf) | [ripgrep](https://github.com/BurntSushi/ripgrep) · [fd](https://github.com/sharkdp/fd) | [broot](https://github.com/Canop/broot) \| [zoxide](https://github.com/ajeetdsouza/zoxide) \| [skim](https://github.com/skim-rs/skim) |
| 📁 File Manager     | [pcmanfm-qt](https://github.com/lxqt/pcmanfm-qt) | [yazi](https://github.com/sxyazi/yazi) |
| 📝 Text Editor      | [zed](https://github.com/zed-industries/zed) · [featherpad](https://github.com/tsujan/FeatherPad) · [micro](https://github.com/zyedidia/micro) · [nano](https://cgit.git.savannah.gnu.org/cgit/nano.git) | [vscode](https://wiki.archlinux.org/title/Visual_Studio_Code) \| [notepadNext](https://github.com/dail8859/NotepadNext) \| [orbiton](https://github.com/xyproto/orbiton) |
| 🌄 Image Viewer     | [oculante](https://github.com/woelper/oculante) |
| 📖 PDF Reader       | [zathura](https://github.com/pwmt/zathura) |
| 🧰 Monitoring  | [btop](https://github.com/aristocratos/btop) · [mission-center](https://gitlab.com/mission-center-devs/mission-center) · [kmon](https://github.com/orhun/kmon) | | [glances](https://github.com/nicolargo/glances) \| [trippy](https://github.com/fujiapple852/trippy) \| [nvtop](https://github.com/Syllo/nvtop) \| [systemd-manager-tui](https://github.com/matheus-git/systemd-manager-tui) \| [pik](https://github.com/jacek-kurlit/pik) |
| 📷 Screenshot       | [wayshot](https://git.sr.ht/~shinyzenith/wayshot) | [grimshot](https://github.com/OctopusET/sway-contrib) \| [shotman](https://git.sr.ht/~whynothugo/shotman) \| [satty](https://github.com/gabm/satty) \| [wayscriber](https://github.com/devmobasa/wayscriber) |
| 📹 Screencast       | [gpu-screen-recorder](https://git.dec05eba.com/gpu-screen-recorder/about/) \| [obs](https://obsproject.com/) | [wf-recorder](https://github.com/ammen99/wf-recorder) |
| 🎚️ Multimedia Control | [playerctl](https://github.com/altdesktop/playerctl) | [easyeffects](https://github.com/wwmm/easyeffects)|
| 🎬 Media Player     | [mpv](https://github.com/mpv-player/mpv) + [yt-dlp](https://github.com/yt-dlp/yt-dlp) |
| 🎵 Audio Player & Visualizer   | [rmpc](https://github.com/mierak/rmpc) ﹢ [cava](https://github.com/karlstav/cava) | [ncspot](https://github.com/hrkfdn/ncspot) | [musializer](https://github.com/tsoding/musializer) |
| 📝 Diff tools  | [meld](https://gitlab.gnome.org/GNOME/meld) |
| 🔧 Misc        | [xdg-ninja](https://github.com/b3nj5m1n/xdg-ninja) |
| 🌧️ Terminal Visuals | [tenki](https://github.com/ckaznable/tenki) · [ascii-rain](https://github.com/nkleemann/ascii-rain) |
| 🗒️ Notes            | [obsidian](https://obsidian.md/) \| [AppFlowy](https://github.com/AppFlowy-IO/AppFlowy) + [notesnook](https://notesnook.com/) \| [planify](https://github.com/alainm23/planify) |
| 🔖 Bookmark Manager | [raindrop](https://raindrop.io/) |

---

## Other
| Module Type | Module Name |
|-------------|-------------|
| Misc. Tools | [arch-update](https://github.com/Antiz96/arch-update) · [neohtop](https://github.com/Abdenasser/neohtop) · [s-tui](https://github.com/amanusk/s-tui) · [netdata](https://github.com/netdata/netdata) · [iotop](https://github.com/Tomas-M/iotop) · [powertop](https://github.com/fenrus75/powertop) · [wavemon](https://github.com/uoaerg/wavemon) · [fselect](https://github.com/jhspetersson/fselect) · [rainfrog](https://github.com/achristmascarl/rainfrog) · [usql](https://github.com/xo/usql) · [delta](https://github.com/dandavison/delta) [wayfreeze](https://github.com/Jappie3/wayfreeze) · [hyprfreeze](https://github.com/Zerodya/hyprfreeze) · [woomer](https://github.com/coffeeispower/woomer) |

---

## 🎨 Theming & Appearance

| Module Type | Module Name |
|-------------|-------------|
| 🎨 Theme Manager | [kvantum](https://github.com/tsujan/Kvantum) + [nwg-look](https://github.com/nwg-piotr/nwg-look) |
| 🌈 GTK Themes    | [libadwaita](https://gitlab.gnome.org/GNOME/libadwaita) \| [nordic](https://github.com/EliverLara/Nordic) \| [whale](https://github.com/anufrievroman/whale) |
| ✨ Qt Themes     | [kvlibadwaita](https://github.com/GabePoel/KvLibadwaita) \| [nordic](https://github.com/EliverLara/Nordic) \| [whale](https://github.com/anufrievroman/whale) |
| 🔤 Fonts         | [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) · [cascadia-code](https://github.com/microsoft/cascadia-code) · [terminus-font](https://archlinux.org/packages/extra/any/terminus-font/) |
| 🔤 Nerd Fonts    | [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) · [cascadia-code](https://github.com/microsoft/cascadia-code) · [terminus-font](https://archlinux.org/packages/extra/any/terminus-font/) |
| 🔠 Emoji         | [bemoji](https://github.com/marty-oehme/bemoji)
| 🧸 Icons         | |

---

```
https://wiki.gentoo.org/wiki/Sway
https://habr.com/ru/articles/484378/
https://fedoraproject.org/wiki/SIGs/Sway
https://gitlab.com/fedora/sigs/sway/sway-config-fedora
https://github.com/alebastr/dotfiles
https://github.com/madic-creates/Sway-DE/blob/master/config/sway/sway.d/01_general.conf
https://valerioviperino.me/sway-fresh-start/
https://claromes.com/blog/customizing-my-micro-editor
https://fig.io/manual/micro
https://forum.garudalinux.org/t/mastering-the-micro-text-editor/32889/13

https://github.com/aceydot/swaydots
https://codeberg.org/stdrice/pengurice
https://taingram.org/blog/sway-tips.html
https://gist.github.com/Ashe/b1bf084206c17e984eb26e63f0fb9f59
https://github.com/topics/sway
https://ctlos.github.io/wiki/wm/sway/
https://github.com/dawsers/scroll - тут описаны полезные настройки Sway и его форка Scroll. Указаны полезные переменные окружения и т.д
```

https://labwc.github.io/hidpi-scaling-patches.html  
https://github.com/snes19xx/EverCal   
