# 🐱 Kitty Terminal Configuration

A clean, minimal, and modern **Kitty terminal configuration** focused on transparency, blur, smooth cursor effects, readable typography, and a polished developer workflow.

<p align="center">
  <img src="screenshots/kitty.png" alt="Kitty Terminal" width="900">
</p>

---

## ✨ Features

* 🌫️ **Transparent background** with dynamic opacity
* 💎 **Blurred terminal background**
* 🔤 **Nerd Font support**
* 🎯 **Beam cursor** with cursor trail
* 📑 **Powerline-style tab bar**
* 📐 Clean window padding and hidden decorations
* 📜 **10,000 lines of scrollback**
* ⚡ Tuned repaint and input delays
* 🎨 Custom high-contrast ANSI color palette
* 🐚 **Zsh** as the default shell
* 🖥️ Optimized for a clean developer environment

---

## 🎨 Appearance

The configuration uses a transparent and blurred terminal background:

```conf
background_opacity 0.75
dynamic_background_opacity yes
background_blur 100
```

The terminal also uses a minimal window layout:

```conf
window_padding_width 14
hide_window_decorations yes
```

This gives Kitty a clean, distraction-free appearance while keeping the terminal visually integrated with the desktop.

---

## 🔤 Fonts

The configuration is designed around **Nerd Fonts**, allowing terminal applications to display icons correctly.

Current font configuration:

```conf
font_family      JetBrainsMono Nerd Font Mono
font_size        12.0
```

The configuration also contains an alternative **FiraCode Nerd Font** setup.

If your font is not installed, install a Nerd Font and change `font_family` to match the font installed on your system.

---

## 🎯 Cursor

The cursor uses a beam style with blinking and a trail effect:

```conf
cursor_shape beam
cursor_blink_interval 0.5
cursor_trail 1
cursor_trail_decay 0.1 0.4
```

This creates a more dynamic cursor while typing.

---

## 📑 Tab Bar

Kitty uses a Powerline-style tab bar positioned at the top:

```conf
tab_bar_edge top
tab_bar_style powerline
tab_powerline_style slanted
```

---

## 🎨 Color Palette

The configuration includes a custom ANSI color palette.

| Color          | Usage                        |
| -------------- | ---------------------------- |
| ⚫ Black / Grey | Base colors                  |
| 🔴 Red         | C files, archives            |
| 🟢 Green       | Executables, scripts         |
| 🟡 Yellow      | Headers, configuration files |
| 🔵 Blue        | Directories                  |
| 🟣 Magenta     | Lua and special files        |
| 🩵 Cyan        | Symbolic links               |
| ⚪ White        | Regular files                |

The colors are defined directly in `kitty.conf` using Kitty's ANSI color settings.

---

## 🐚 Shell

The default shell is **Zsh**:

```conf
shell zsh
```

This configuration is intended to work well alongside a customized Zsh environment.

---

## ⚡ Performance

The configuration includes several settings intended to keep terminal input and rendering responsive:

```conf
repaint_delay 8
input_delay 2
sync_to_monitor yes
```

Scrollback is also configured for:

```conf
scrollback_lines 10000
wheel_scroll_multiplier 3.0
```

---

## 📦 Installation

### 1. Install Kitty

Install Kitty using your distribution's package manager.

### 2. Clone the configuration

Clone this repository:

```bash
git clone https://github.com/DR-C002/kitty-config.git
```

Then copy or link the configuration to Kitty's configuration directory:

```bash
mkdir -p ~/.config/kitty
cp kitty.conf ~/.config/kitty/kitty.conf
```

Or, if you want the repository itself to be your active configuration:

```bash
ln -sf "$(pwd)/kitty.conf" ~/.config/kitty/kitty.conf
```

### 3. Restart Kitty

Close and reopen Kitty to apply the configuration.

---

## 📁 Configuration

The main configuration file is:

```text
kitty-config/
└── kitty.conf
```

---

## 🖼️ Screenshots

<p align="center">
  <img src="screenshots/kitty.png" alt="Kitty configuration" width="900">
</p>

Add additional screenshots here if you want to showcase different parts of the setup.

---

## 🛠️ Customization

The configuration is intentionally easy to modify.

### Change font

```conf
font_family Your Nerd Font
font_size 12.0
```

### Change transparency

```conf
background_opacity 0.75
```

### Change blur

```conf
background_blur 100
```

### Change padding

```conf
window_padding_width 14
```

All of these settings are defined directly in `kitty.conf`.

---

## 📌 Requirements

* [Kitty](https://sw.kovidgoyal.net/kitty/)
* Zsh
* A Nerd Font

---

## 📄 License

Feel free to use, modify, and adapt this configuration for your own setup.

---

<p align="center">
  Made with 🐧 + 🐱 + ❤️
</p>
