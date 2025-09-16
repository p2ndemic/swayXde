<img width=150 height=50 align=right src="https://archlinux.org/static/logos/archlinux-logo-light-1200dpi.7ccd81fd52dc.png">

# swayXde
My attempt to create a desktop environment for Sway


## 🖥️ OS & Core Components

| Module Type | Module Name | Optional |
|-------------|-------------|----------|
| 🧰 Operating System          | [Arch Linux](https://archlinux.org/) \| [CachyOS](https://cachyos.org/)
| 🔹 Intel Drivers             | [intel-ucode](https://archlinux.org/packages/extra/any/intel-ucode/) + [vulkan-intel](https://archlinux.org/packages/extra/x86_64/vulkan-intel) + [vulkan-icd-loader](https://archlinux.org/packages/extra/x86_64/vulkan-icd-loader/) + [vulkan-headers](https://archlinux.org/packages/extra/any/vulkan-headers/) + [vulkan-mesa-layers](https://archlinux.org/packages/extra/x86_64/vulkan-mesa-layers/) + [vulkan-tools](https://archlinux.org/packages/extra/x86_64/vulkan-tools/) + [intel-compute-runtime](https://archlinux.org/packages/extra/x86_64/intel-compute-runtime/) + [opencl-icd-loader](https://aur.archlinux.org/packages/opencl-icd-loader) + [intel-media-driver](https://archlinux.org/packages/extra/x86_64/intel-media-driver/) + [vpl-gpu-rt](https://archlinux.org/packages/extra/x86_64/vpl-gpu-rt/) | [ocl-icd](https://archlinux.org/packages/extra/x86_64/ocl-icd/) \| [level-zero-loader](https://archlinux.org/packages/extra/x86_64/level-zero-loader/) \| [level-zero-headers](https://archlinux.org/packages/extra/x86_64/level-zero-headers/) |
| 🔸 AMD Drivers               | [amd-ucode](https://archlinux.org/packages/core/any/amd-ucode) + [vulkan-radeon](https://archlinux.org/packages/extra/x86_64/vulkan-radeon/) + [vulkan-icd-loader](https://archlinux.org/packages/extra/x86_64/vulkan-icd-loader/) + [vulkan-headers](https://archlinux.org/packages/extra/any/vulkan-headers/) + [vulkan-mesa-layers](https://archlinux.org/packages/extra/x86_64/vulkan-mesa-layers/) + [vulkan-tools](https://archlinux.org/packages/extra/x86_64/vulkan-tools/) + [opencl-icd-loader](https://aur.archlinux.org/packages/opencl-icd-loader) + [mesa](https://archlinux.org/packages/extra/x86_64/mesa/) |
| ⚡ Power tuning daemon       | [tuned](https://github.com/redhat-performance/tuned) + [tuned-gui](https://github.com/redhat-performance/tuned) |
| 🔋 Power Alert Daemon        | [poweralertd](https://sr.ht/~kennylevinsen/poweralertd/) |
| 📶 Network Management tool   | [networkmanager](https://networkmanager.dev/) + [nm-connection-editor](https://gitlab.gnome.org/GNOME/network-manager-applet) |
| 📡 Bluetooth Management tool | [blueman](https://github.com/blueman-project/blueman) |
| 🔊 Piperwire volume control tool | [pwvucontrol](https://github.com/saivert/pwvucontrol) |
| 🧊 Idle Daemon               | [swayidle](https://github.com/swaywm/swayidle) |

---

## 🖼️ Display Managers & Wayland Stack

| Module Type | Module Name | Alternatives |
|-------------|-------------|--------------|
| 🚪 Display Manager        | [ly](https://codeberg.org/fairyglade/ly) | [gdm](https://gitlab.gnome.org/GNOME/gdm.git) \| [greetd](https://git.sr.ht/~kennylevinsen/greetd) + [regreet](https://github.com/rharish101/ReGreet) |
| 🪟 Wayland Compositor     | [sway](https://github.com/swaywm/sway) |
| 📜 Wayland Protocols      | [wayland-protocols](https://gitlab.freedesktop.org/wayland/wayland-protocols) + [wlr-protocols](https://gitlab.freedesktop.org/wlroots/wlr-protocols) + [frog-protocols](https://github.com/misyltoad/frog-protocols) |
| 🔐 Session Access Manager | [polkit](https://github.com/polkit-org/polkit) |
| 🌀 Portal Backend         | [xdg-desktop-portal-wlr](https://github.com/emersion/xdg-desktop-portal-wlr) |
| 🧩 Qt Wayland Modules     | [qt5-wayland](https://archlinux.org/packages/extra/x86_64/qt5-wayland) + [qt6-wayland](https://archlinux.org/packages/extra/x86_64/qt6-wayland) |

---

## 📟 Terminal & Shell

| Module Type | Module Name | Alternatives |
|-------------|-------------|--------------|
| 🐟 Shell & Framework | [fish](https://github.com/fish-shell/fish-shell) + [oh-my-fish](https://github.com/oh-my-fish/oh-my-fish) |
| 💫 Shell Enhancers   | [starship](https://github.com/starship/starship) \| [navi](https://github.com/denisidoro/navi) | [oh-my-posh](https://github.com/JanDeDobbeleer/oh-my-posh) |
| 🖥️ Terminal Emulator | [foot](https://codeberg.org/dnkl/foot) |
| 🔧 Terminal Tools    | [eza](https://github.com/eza-community/eza) \| [bat](https://github.com/sharkdp/bat)
| 🔍 File Search Tools | [fzf](https://github.com/junegunn/fzf) \| [ripgrep](https://github.com/BurntSushi/ripgrep) \| [fd](https://github.com/sharkdp/fd) | [skim](https://github.com/skim-rs/skim)
| 📈 System Fetch      | [fastfetch](https://github.com/fastfetch-cli/fastfetch) |

---

## 🧩 Workspace Tools

| Module Type | Module Name | Alternatives |
|-------------|-------------|--------------|
| 🧱 Bar / Panel         | [waybar](https://github.com/Alexays/Waybar) | [ironbar](https://github.com/JakeStanger/ironbar) |
| 💡 OSD                 | [swayosd](https://github.com/ErikReider/SwayOSD)
| 🔔 Notification Daemon | [fnott](https://codeberg.org/dnkl/fnott) \| [mako](https://github.com/emersion/mako) | [SwayNotificationCenter](https://github.com/ErikReider/SwayNotificationCenter)
| 🎚️ Brightness & Gamma  | [brightnessctl](https://github.com/Hummer12007/brightnessctl) | [gammastep](https://gitlab.com/chinstrap/gammastep) \| [wlsunset](https://git.sr.ht/~kennylevinsen/wlsunset) |
| 🖼️ Wallpaper Tools     | [swaybg](https://github.com/swaywm/swaybg) | [wpaperd](https://github.com/danyspin97/wpaperd) \| [wallutils](https://github.com/xyproto/wallutils) |
| 🔒 Lockscreen & Logout | [swaylock](https://github.com/swaywm/swaylock) + [wleave](https://github.com/AMNatty/wleave) | [waylock](https://codeberg.org/ifreund/waylock) |
| 🧰 Configuration Tools | [swaysettings](https://github.com/ErikReider/SwaySettings) + [nwg-displays](https://github.com/nwg-piotr/nwg-displays) |
| 📺 Output Config Tools | [kanshi](https://sr.ht/~emersion/kanshi) | [wlr-randr](https://gitlab.freedesktop.org/emersion/wlr-randr) \| [shikane](https://gitlab.com/w0lff/shikane) |

---

## 🧰 Utilities & System Tools

| Module Type | Module Name |
|-------------|-------------|
| 📊 Monitoring & Metrics  | [btop](https://github.com/aristocratos/btop) \| [glances](https://github.com/nicolargo/glances) \| [netdata](https://github.com/netdata/netdata) \| [nvtop](https://github.com/Syllo/nvtop) \| [s-tui](https://github.com/amanusk/s-tui) \| [neohtop](https://github.com/Abdenasser/neohtop) \| [mission-center](https://gitlab.com/mission-center-devs/mission-center) |
| 💻 System Utilities      | [iotop](https://github.com/Tomas-M/iotop) \| [kmon](https://github.com/orhun/kmon) \| [systemd-manager-tui](https://github.com/matheus-git/systemd-manager-tui) \| [powertop](https://github.com/fenrus75/powertop) \| [acpid](https://wiki.archlinux.org/title/Acpid) |
| 🧠 Info & Diagnostics    | [inxi](https://codeberg.org/smxi/inxi) \| [duf](https://github.com/muesli/duf) \| [wavemon](https://github.com/uoaerg/wavemon) \| [iftop](https://code.blinkace.com/pdw/iftop) |
| 📁 Disk & File Tools     | [dua-cli](https://github.com/Byron/dua-cli) \| [fselect](https://github.com/jhspetersson/fselect) \| [broot](https://github.com/Canop/broot) |
| 📚 Knowledge Tools       |  \| [xdg-ninja](https://github.com/b3nj5m1n/xdg-ninja) |
| 🧊 Misc                  | [wayfreeze](https://github.com/Jappie3/wayfreeze) \| [hyprfreeze](https://github.com/Zerodya/hyprfreeze) \| [vigiland](https://github.com/Jappie3/vigiland) \| [planify](https://github.com/alainm23/planify) \| [resources](https://github.com/nokyan/resources) \| [arch-update](https://github.com/Antiz96/arch-update) |
| 🔧 Misc. Tools           | [wluma](https://github.com/maximbaz/wluma) \| [laptop-mode-tools](https://github.com/rickysarraf/laptop-mode-tools) \| [thermald](https://github.com/intel/thermal_daemon) |
| 📦 Others                | [usql](https://github.com/xo/usql) \| [jq](https://jqlang.org/) \| [pik](https://github.com/jacek-kurlit/pik) \| [woomer](https://github.com/coffeeispower/woomer) |

---

## 📋 Clipboard, Notifications, Input

| Module Type | Module Name |
|-------------|-------------|
| 🗂️ Clipboard Manager   | [wl-clipboard-rs](https://github.com/YaLTeR/wl-clipboard-rs) \| [cliphist](https://github.com/sentriz/cliphist) \| [clipse](https://github.com/savedra1/clipse) \| [clipvault](https://github.com/rolv-apneseth/clipvault) |
| 🔠 Emoji Picker        | [bemoji](https://github.com/marty-oehme/bemoji)                             |

---

## 📦 Applications

| Module Type | Module Name | Alternatives |
|-------------|-------------|--------------|
| 🚀 App Launcher          | [fuzzel](https://codeberg.org/dnkl/fuzzel) \| [walker](https://github.com/abenz1267/walker) |
| 📁 File Managers         | [pcmanfm-qt](https://github.com/lxqt/pcmanfm-qt) \| [nautilus](https://wiki.gnome.org/Apps/Files) \| [yazi](https://github.com/sxyazi/yazi) |
| 📝 Text Editors          | [zed](https://github.com/zed-industries/zed) \| [vscode](https://wiki.archlinux.org/title/Visual_Studio_Code) \| [micro](https://github.com/zyedidia/micro) \| [orbiton](https://github.com/xyproto/orbiton) \| [nano](https://cgit.git.savannah.gnu.org/cgit/nano.git) |
| 📸 Screenshot Tools      | [wayshot](https://git.sr.ht/~shinyzenith/wayshot) | [grimshot](https://github.com/OctopusET/sway-contrib) \| [shotman](https://git.sr.ht/~whynothugo/shotman) \| [satty](https://github.com/gabm/satty) |
| 🎥 Screen Recording      | [wl-screenrec](https://github.com/russelltg/wl-screenrec) \| [gpu-screen-recorder](https://git.dec05eba.com/gpu-screen-recorder/about/) \| [obs](https://obsproject.com/) |
| 🎚️ Multimedia Control Tools | [playerctl](https://github.com/altdesktop/playerctl) | [easyeffects](https://github.com/wwmm/easyeffects)|
| 🎬 Media Players         | [mpv](https://github.com/mpv-player/mpv) + [yt-dlp](https://github.com/yt-dlp/yt-dlp) |
| 🎵 Audio Players         | [rmpc](https://github.com/mierak/rmpc) + [ncspot](https://github.com/hrkfdn/ncspot) /
| 📊 Audio Visualizer      | [cava](https://github.com/karlstav/cava) \| [musializer](https://github.com/tsoding/musializer) |
| 📖 PDF Reader            | [zathura](https://github.com/pwmt/zathura)                                  |
| 🖼️ Image Viewer          | [oculante](https://github.com/woelper/oculante)                             |
| ⏰ Clock                 | [tenki](https://github.com/ckaznable/tenki)                                 |

| 🌧️ Terminal Visuals      | [ascii-rain](https://github.com/nkleemann/ascii-rain)                       |
| 🗒️ Notes                 | [obsidian](https://obsidian.md/) \| [AppFlowy](https://github.com/AppFlowy-IO/AppFlowy) + [notesnook](https://notesnook.com/) |
| 🔖 Bookmark Manager      | [raindrop](https://raindrop.io/)                                            |

---

## 🎨 Theming & Appearance

| Module Type | Module Name |
|-------------|-------------|
| 🎨 Theme Manager | [kvantum](https://github.com/tsujan/Kvantum) + [nwg-look](https://github.com/nwg-piotr/nwg-look) |
| 🌈 GTK Themes    | [libadwaita](https://gitlab.gnome.org/GNOME/libadwaita) \| [nordic](https://github.com/EliverLara/Nordic) \| [whale](https://github.com/anufrievroman/whale) |
| ✨ Qt Themes     | [kvlibadwaita](https://github.com/GabePoel/KvLibadwaita) \| [nordic](https://github.com/EliverLara/Nordic) \| [whale](https://github.com/anufrievroman/whale) |
| 🧸 Icons         | [Papirus Dark](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme) |
| 🔤 Fonts         | [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) |

---
