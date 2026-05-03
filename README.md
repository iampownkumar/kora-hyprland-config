# Kora Hyprland Config

Personal Hyprland configuration used on **Arch Linux**.

Maintained by **Pownkumar — Founder of Korelium**
Create on	 : March 2 2026
Last Update on   : May 3 2026
---

## Overview

This repository contains a **modular Hyprland configuration** designed for a clean and keyboard-driven workflow.

The configuration separates different components into dedicated files to improve maintainability and readability.

---

## Features

- Modular Hyprland configuration
- ALT used as the main modifier key (keyboard issue with Super key)
- Workspace based navigation
- VIM-style window movement (H J K L)
- Screenshot workflow using `grim` and `slurp`
- Volume and brightness keybindings
- Waybar status bar integration

---

## Configuration Structure

hypr/

* hyprland.conf
* variables.conf
* monitors.conf
* input.conf
* appearance.conf
* keybinds.conf
* autostart.conf

---

## Key Design Choices

### ALT as Main Modifier

The system uses **ALT as `$mainMod`** because the keyboard Super key is currently faulty.

```ini
$mainMod = ALT
```

This can easily be changed later in `variables.conf`.

---

### Modular Configuration

Instead of a single large config file, the setup uses multiple focused configuration files:

```
hypr/
├── hyprland.conf
├── variables.conf
├── monitors.conf
├── input.conf
├── appearance.conf
├── keybinds.conf
└── autostart.conf
```

This makes the configuration easier to debug and maintain.

---

## Dependencies

Typical packages used with this setup:

```
hyprland
waybar
wofi
dunst
grim
slurp
wl-clipboard
brightnessctl
pipewire
playerctl
nm-applet
blueman
hyprlock
```

---

## Quick Setup (Arch Linux)

If you're on **Arch Linux** and just want to get things running quickly, copy and paste this command in your terminal:

```bash
sudo pacman -S hyprland waybar wofi dunst grim slurp wl-clipboard brightnessctl playerctl network-manager-applet blueman hyprlock kitty dolphin konsole
```

Grab a coffee ☕ while pacman does its thing.

This installs everything needed for the core experience:

* **Hyprland** → Window manager
* **Waybar** → Top status bar
* **Wofi** → Application launcher
* **Dunst** → Notifications
* **Grim + Slurp** → Screenshots
* **wl-clipboard** → Clipboard support
* **Brightnessctl** → Brightness controls
* **Playerctl** → Media controls
* **Network Manager Applet** → Wi-Fi manager
* **Blueman** → Bluetooth manager
* **Hyprlock** → Screen lock
* **Kitty / Konsole** → Terminal options
* **Dolphin** → File manager

After installation, clone the config and you're ready to go 🚀


---


## Screenshot Workflow

Full Screenshot:

```
Print
```

Area Screenshot:

```
Shift + Print
```

Screenshots are saved to:

```
~/Pictures/
```

and copied to clipboard automatically.

---

## Installation

Clone the repository:

git clone https://github.com/iampownkumar/hypr.git 

Copy the configuration:

cp -r kora-hyprland-config/* ~/.config/hypr/

Reload Hyprland:

hyprctl reload

Then link it to your Hyprland config directory.

---

## Philosophy

The goal of this configuration is to keep the system:

- minimal
- modular
- keyboard-driven
- easy to maintain

---

Arch Linux • Hyprland • Wayland
