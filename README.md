<img width=150 height=50 align=left src="https://swaywm.org/logo.png">
<img width=150 height=50 align=right src="https://archlinux.org/static/logos/archlinux-logo-light-1200dpi.7ccd81fd52dc.png">

<br><br>

<h1 align="center">swayXde</h1>

<h6 align="right"><em>My attempt to create a desktop environment for Sway</em></h1>



## 🖥️ OS & Core Components

| Module Type | Module Name |
|-------------|-------------|
| 💻 Operating System          | [Arch Linux](https://archlinux.org/) |
| 🐧 Kernel                    | [linux-prjc-lfbmq](https://gitlab.com/alfredchen/linux-prjc/-/tree/linux-6.17.y-prjc-lfbmq) · _[Test](https://www.reddit.com/r/linux_gaming/comments/1nkg0lr/update_on_my_bmq_scheduler_post_a_sidebyside/)_ |
| ⚡ Power tuning daemon       | [tuned](https://github.com/redhat-performance/tuned) ﹢ [tuned-gui](https://github.com/redhat-performance/tuned) |
| 🔋 Power Alert Daemon        | [poweralertd](https://sr.ht/~kennylevinsen/poweralertd/) |
| 📶🌐 Network Management tool | [networkmanager](https://networkmanager.dev/) ﹢ [nm-connection-editor](https://archlinux.org/packages/extra/x86_64/nm-connection-editor/) |
| 📡 Bluetooth Management tool | [blueman](https://github.com/blueman-project/blueman) |
| 🔊 Piperwire volume control tool | [pwvucontrol](https://github.com/saivert/pwvucontrol) |
| 🌙 Idle Daemon               | [swayidle](https://github.com/swaywm/swayidle) |
| 🅰️ Font rendering            | [fontconfig](https://archlinux.org/packages/extra/x86_64/fontconfig/) · [freetype2](https://archlinux.org/packages/extra/x86_64/freetype2/) |
| 🧊 Archiving & Compression   | [libarchive](https://archlinux.org/packages/core/x86_64/libarchive/) · [7zip](https://archlinux.org/packages/extra/x86_64/7zip/) · [arqiver](https://aur.archlinux.org/packages/arqiver) |
|[chaotic-aur](https://aur.chaotic.cx/)|

## 📦 Drivers & Firmware

| Module Type | Module Name | Optional | Note |
|-------------|-------------|----------|------|
| ⚙️ Linux Firmware       | [linux-firmware](https://archlinux.org/packages/core/any/linux-firmware/) · [sof-firmware](https://archlinux.org/packages/extra/x86_64/sof-firmware/) |
| 🧰 Mesa Stack           | [mesa](https://archlinux.org/packages/extra/x86_64/mesa/) | |
| 📡 Bluetooth drivers    | [bluez](https://wiki.archlinux.org/title/Bluetooth) · [bluez-libs](https://archlinux.org/packages/extra/x86_64/bluez-libs/) · [bluez-utils](https://archlinux.org/packages/extra/x86_64/bluez-utils/) | [bluez-hid2hci](https://archlinux.org/packages/extra/x86_64/bluez-hid2hci/) | _sudo usermod -aG lp $USER && sudo systemctl enable --now bluetooth.service_ |

### 🔹 Intel Drivers

| Module Type | Module Name | Optional | Note |
|-------------|-------------|----------|------|
| 🔹 Intel Microcode | [intel-ucode](https://archlinux.org/packages/extra/any/intel-ucode/) |
| 🔹 Intel Vulkan    | [vulkan-intel](https://archlinux.org/packages/extra/x86_64/vulkan-intel) · [vulkan-icd-loader](https://archlinux.org/packages/extra/x86_64/vulkan-icd-loader/) · [vulkan-headers](https://archlinux.org/packages/extra/any/vulkan-headers/) · [vulkan-mesa-layers](https://archlinux.org/packages/extra/x86_64/vulkan-mesa-layers/) · [vulkan-tools](https://archlinux.org/packages/extra/x86_64/vulkan-tools/) · [mesa-utils](https://archlinux.org/packages/extra/x86_64/mesa-utils/) |
| 🔹 Intel OpenCL    | [intel-compute-runtime](https://archlinux.org/packages/extra/x86_64/intel-compute-runtime/) · [opencl-icd-loader](https://aur.archlinux.org/packages/opencl-icd-loader) | [ocl-icd](https://archlinux.org/packages/extra/x86_64/ocl-icd/) | _env OCL_ICD_VENDORS=/etc/OpenCL/vendors/intel.icd_ |
| 🔹 Intel VA-API    | [intel-media-driver](https://archlinux.org/packages/extra/x86_64/intel-media-driver/) · [vpl-gpu-rt](https://archlinux.org/packages/extra/x86_64/vpl-gpu-rt/) · [libvpl-tools](https://archlinux.org/packages/extra/x86_64/libvpl-tools/) | | _[Arch Wiki](https://wiki.archlinux.org/title/Hardware_video_acceleration)_ |
| 1️⃣ oneAPI          | _optional_ | [level-zero-loader](https://archlinux.org/packages/extra/x86_64/level-zero-loader/) · [level-zero-headers](https://archlinux.org/packages/extra/x86_64/level-zero-headers/) |

### 🔸 AMD Drivers

| Module Type | Module Name | Optional | Note |
|-------------|-------------|----------|------|
| 🔸 AMD Microcode | [amd-ucode](https://archlinux.org/packages/core/any/amd-ucode) |
| 🔸 AMD Vulkan    | [vulkan-radeon](https://archlinux.org/packages/extra/x86_64/vulkan-radeon/) · [vulkan-icd-loader](https://archlinux.org/packages/extra/x86_64/vulkan-icd-loader/) · [vulkan-headers](https://archlinux.org/packages/extra/any/vulkan-headers/) · [vulkan-mesa-layers](https://archlinux.org/packages/extra/x86_64/vulkan-mesa-layers/) · [vulkan-tools](https://archlinux.org/packages/extra/x86_64/vulkan-tools/) · [mesa-utils](https://archlinux.org/packages/extra/x86_64/mesa-utils/) |
| 🔸 AMD OpenCL    | [opencl-mesa](https://archlinux.org/packages/extra/x86_64/opencl-mesa/) · [opencl-icd-loader](https://aur.archlinux.org/packages/opencl-icd-loader) | [rocm-opencl-runtime](https://archlinux.org/packages/extra/x86_64/rocm-opencl-runtime/) \| [ocl-icd](https://archlinux.org/packages/extra/x86_64/ocl-icd/) | _env RUSTICL_ENABLE=radeonsi_ |
| 🔸 AMD VA-API    | [mesa](https://archlinux.org/packages/extra/x86_64/mesa/) | | _[Arch Wiki](https://wiki.archlinux.org/title/Hardware_video_acceleration)_ |

---

## 🖼️ Display Managers & Wayland Stack

| Module Type | Module Name | Alternatives |
|-------------|-------------|--------------|
| 🚪 Display Manager        | [ly](https://codeberg.org/fairyglade/ly) | [greetd](https://git.sr.ht/~kennylevinsen/greetd) ﹢ [regreet](https://github.com/rharish101/ReGreet) |
| 🪟 Wayland Compositor     | [sway](https://github.com/swaywm/sway) |
| 📜 Wayland Protocols      | [wayland-protocols](https://gitlab.freedesktop.org/wayland/wayland-protocols) ﹢ [wlr-protocols](https://gitlab.freedesktop.org/wlroots/wlr-protocols) + [frog-protocols](https://github.com/misyltoad/frog-protocols) |
| 🛰️ EGL Wayland & XWayland | [egl-wayland](https://archlinux.org/packages/extra/x86_64/egl-wayland/) · [xorg-xwayland](https://archlinux.org/packages/extra/x86_64/xorg-xwayland/)
| 🧩 Qt Wayland Modules     | [qt5-wayland](https://archlinux.org/packages/extra/x86_64/qt5-wayland) · [qt6-wayland](https://archlinux.org/packages/extra/x86_64/qt6-wayland) |
| 🔐 Session Access Manager | [polkit](https://wiki.archlinux.org/title/Polkit) · [lxqt-policykit](https://archlinux.org/packages/extra/x86_64/lxqt-policykit/)
| 🌀 XDG Portal Backend     | [xdg-desktop-portal](https://wiki.archlinux.org/title/XDG_Desktop_Portal) · [xdg-desktop-portal-wlr](https://archlinux.org/packages/extra/x86_64/xdg-desktop-portal-wlr/) · [xdg-desktop-portal-lxqt](https://archlinux.org/packages/extra/x86_64/xdg-desktop-portal-lxqt/)
| 🗂️ XDG User Dirs & Utils  | [xdg-user-dirs](https://wiki.archlinux.org/title/XDG_user_directories) · [xdg-utils](https://wiki.archlinux.org/title/Xdg-utils)

---

## 📟 Terminal & Shell

| Module Type | Module Name | Alternatives |
|-------------|-------------|--------------|
| 🐟 Shell & Framework     | [fish](https://github.com/fish-shell/fish-shell) ﹢ [oh-my-fish](https://github.com/oh-my-fish/oh-my-fish) |
| 💫 Shell Enhancers       | [starship](https://github.com/starship/starship) \| [navi](https://github.com/denisidoro/navi) | [oh-my-posh](https://github.com/JanDeDobbeleer/oh-my-posh) |
| 🖥️ Terminal Emulator     | [foot](https://codeberg.org/dnkl/foot) |
| 🔧 Terminal Tools        | [eza](https://github.com/eza-community/eza) \| [bat](https://github.com/sharkdp/bat) | [broot](https://github.com/Canop/broot) \| [zoxide](https://github.com/ajeetdsouza/zoxide) |
| 🔍 File Search Tools     | [fzf](https://github.com/junegunn/fzf) \| [ripgrep](https://github.com/BurntSushi/ripgrep) \| [fd](https://github.com/sharkdp/fd) | [skim](https://github.com/skim-rs/skim)
| 💾 Disk Usage & Cleaning | [duf](https://github.com/muesli/duf) | [dua-cli](https://github.com/Byron/dua-cli)
| 📈 System Fetch & Info   | [fastfetch](https://github.com/fastfetch-cli/fastfetch) · [inxi](https://codeberg.org/smxi/inxi) |
| 📝 Diff and merge tools  | [meld](https://gitlab.gnome.org/GNOME/meld)

---

## 🧩 Workspace Tools

| Module Type | Module Name | Alternatives |
|-------------|-------------|--------------|
| 🧱 Bar / Panel         | [waybar](https://github.com/Alexays/Waybar) | [ironbar](https://github.com/JakeStanger/ironbar) \| [eww](https://github.com/elkowar/eww) |
| 💡 OSD                 | [swayosd](https://github.com/ErikReider/SwayOSD)
| 🔔 Notification Daemon | [fnott](https://codeberg.org/dnkl/fnott) \| [mako](https://github.com/emersion/mako) | [SwayNotificationCenter](https://github.com/ErikReider/SwayNotificationCenter)
| 🎚️ Brightness & Gamma  | [brightnessctl](https://github.com/Hummer12007/brightnessctl) | [gammastep](https://gitlab.com/chinstrap/gammastep) \| [wlsunset](https://git.sr.ht/~kennylevinsen/wlsunset) |
| 🖼️ Wallpaper Tools     | [swaybg](https://github.com/swaywm/swaybg) | [wpaperd](https://github.com/danyspin97/wpaperd) \| [wallutils](https://github.com/xyproto/wallutils) \| [swww](https://github.com/LGFae/swww) |
| 🔒 Lockscreen & Logout | [swaylock](https://github.com/swaywm/swaylock) + [wleave](https://github.com/AMNatty/wleave) | [waylock](https://codeberg.org/ifreund/waylock) |
| 🧰 Configuration Tools | [swaysettings](https://github.com/ErikReider/SwaySettings) + [nwg-displays](https://github.com/nwg-piotr/nwg-displays) |
| 📺 Output Config Tools | [kanshi](https://sr.ht/~emersion/kanshi) | [wlr-randr](https://gitlab.freedesktop.org/emersion/wlr-randr) \| [shikane](https://gitlab.com/w0lff/shikane) |
| 🔌 Auto-mount Tools    | [udiskie](https://github.com/coldfix/udiskie)


---

## 🧰 Utilities & System Tools

| Module Type | Module Name |
|-------------|-------------|
| 📊 Monitoring & Metrics  | [btop](https://github.com/aristocratos/btop) \| [glances](https://github.com/nicolargo/glances) \| [netdata](https://github.com/netdata/netdata) \| [nvtop](https://github.com/Syllo/nvtop) \| [s-tui](https://github.com/amanusk/s-tui) \| [neohtop](https://github.com/Abdenasser/neohtop) \| [mission-center](https://gitlab.com/mission-center-devs/mission-center) |
| 💻 System Utilities      | [iotop](https://github.com/Tomas-M/iotop) \| [kmon](https://github.com/orhun/kmon) \| [systemd-manager-tui](https://github.com/matheus-git/systemd-manager-tui) \| [powertop](https://github.com/fenrus75/powertop) \| |
| 🧠 Info & Diagnostics    | [wavemon](https://github.com/uoaerg/wavemon) \| [iftop](https://code.blinkace.com/pdw/iftop) |
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
| 🎨 Theme Manager  | [kvantum](https://github.com/tsujan/Kvantum) + [nwg-look](https://github.com/nwg-piotr/nwg-look) |
| 🌈 GTK Themes     | [libadwaita](https://gitlab.gnome.org/GNOME/libadwaita) \| [nordic](https://github.com/EliverLara/Nordic) \| [whale](https://github.com/anufrievroman/whale) |
| ✨ Qt Themes      | [kvlibadwaita](https://github.com/GabePoel/KvLibadwaita) \| [nordic](https://github.com/EliverLara/Nordic) \| [whale](https://github.com/anufrievroman/whale) |
| 🧸 Icons          | [Papirus Dark](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme) |
| 🔤 Fonts          | [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) |

---

```
https://github.com/aceydot/swaydots
https://codeberg.org/stdrice/pengurice
https://taingram.org/blog/sway-tips.html
```
🔄


✨ Подходящие эмодзи:
Эмодзи	Значение / Обоснование
🧬	"DNA" — слияние, сравнение различий (отлично передаёт идею merge/diff)
🔀	"Twisted arrows" — merge, разветвление, объединение
🔎	"Magnifying glass" — просмотр различий
🪄	"Magic wand" — автоматическое слияние, умный diff (актуально для difftastic, delta)
⚖️	"Scales" — сравнение / выбор между двумя сторонами
🪢	"Knot" — конфликт, который надо развязать (merge conflict)
📝	"Writing" — редактирование во время сравнения
📄	"Document" — работа с файлами (в контексте diff/merge)
✅ Рекомендованный вариант:
| 🧬 Diff & Merge Tools | diff + vimdiff + meld + kdiff3 + delta + difftastic |

Альтернативы:

🔀 — акцент на слияние (merge)

🔎 — акцент на визуальное сравнение

⚖️ — акцент на выбор между версиями

🪢 — если хочешь немного юмора/креативности про merge-конфликты 😅


🌙 — полумесяц (луна)
🌕 — полная луна
🌑 — новолуние
🌛 — улыбающаяся луна (в фазе растущей луны)
🌜 — улыбающаяся луна (в фазе убывающей луны)
🌌 — звёздное небо
⭐ — звезда
🌠 — падающая звезда
😴 — спящий смайлик
💤 — символ сна (звуки "ззз")
🛌 — человек в кровати
🛏️ — кровать
🌃 — ночной город
🪐 — планета (можно для космической тематики сна)

❄️ — снег
🌨️ — снежная погода
🧊 — лёд
🏔️ — заснеженные горы
🌬️ — ветер (морозная атмосфера)
🧣🧤 — шарф и варежки (зимняя одежда, в тему пингвинов)
