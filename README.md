# 🔔 dunst — Lightweight and Customizable Notification Daemon for Linux

**dunst** is a minimal and highly configurable notification daemon for the Linux desktop, designed to work well with lightweight window managers like i3, Openbox, and bspwm. It displays system notifications in a clean, unobtrusive way.

---

## ✅ Features

* Lightweight and fast, minimal dependencies
* Highly customizable appearance (fonts, colors, geometry)
* Supports multiple notification levels with different styles
* Configurable notification timeouts and history
* Supports actions and clickable notifications
* Works smoothly with D-Bus and standard Linux notification systems
* Written in C for efficiency

---

## 🔧 Installation

### Debian / Ubuntu

```bash
sudo apt install dunst
```

### Arch Linux

```bash
sudo pacman -S dunst
```

### Fedora

```bash
sudo dnf install dunst
```

---

## 🚀 Basic Usage

Start dunst in the background:

```bash
dunst &
```

You can add this to your i3 config or your X session startup file (`~/.xinitrc` or `~/.config/i3/config`):

```bash
exec --no-startup-id dunst
```

---

## ⚙️ Configuration

dunst is configured via a plain text config file (usually located at `~/.config/dunst/dunstrc`).

Example configuration options include:

| Option        | Description                                                     |
| ------------- | --------------------------------------------------------------- |
| `geometry`    | Position and size of notification popup (e.g., `300x5-10+40`)   |
| `timeout`     | Time (in milliseconds) before notification closes automatically |
| `font`        | Font family and size (e.g., `Monospace 10`)                     |
| `foreground`  | Text color                                                      |
| `background`  | Background color                                                |
| `frame_color` | Border color                                                    |
| `critical`    | Style for critical notifications                                |

You can customize colors per urgency level (low, normal, critical) for more control.

---

## 🎯 Examples

### Start dunst with default settings

```bash
dunst &
```

### Reload dunst config without restarting

```bash
pkill -SIGUSR1 dunst
```

### Send a test notification (using `notify-send`)

```bash
notify-send "Hello" "This is a test notification"
```

---

## 📚 More Info

* Manual:

```bash
man dunst
```

* GitHub repository: [https://github.com/dunst-project/dunst](https://github.com/dunst-project/dunst)
* Arch Wiki: [https://wiki.archlinux.org/title/Dunst](https://wiki.archlinux.org/title/Dunst)

---

## 🧩 Alternatives

* `mako` — Lightweight Wayland notification daemon
* `notify-osd` — Simple notification daemon for Ubuntu
* `xfce4-notifyd` — Notification daemon for XFCE desktop
