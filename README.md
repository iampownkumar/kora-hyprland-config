# hypr

My personal Hyprland config for Arch Linux. It's modular — each part of the setup lives in its own file so it's easier to tweak without breaking everything else.

---

## Why I made this

Back in 2017, the Tamil Nadu Government gave out laptops to students. I got one — 8GB RAM on paper, but Windows was eating 4 to 4.5GB of that just sitting idle. The laptop was basically dead. I couldn't do anything properly on it.

That's when I decided I'm not living like this. I heard about Linux, and I thought — if Windows is killing my machine, let me try something else. So I did. I started exploring every distro I could find. Tried everything. Eventually landed on Arch, and stayed there.

For years I ran KDE Plasma. It was great. But honestly I got too comfortable, and for me that's a sign to move on. I like problems. I like figuring things out. When things just work without me having to think, I get bored.

That's when I found Hyprland. People were talking about it. I tried it. It was actually worth it — smooth, fast, completely in my control.

This config is mine. It's what runs on my machine right now. The ALT key as the main modifier is there because my Super key broke and I just worked around it. Nothing fancy, nothing polished for the internet. I'm keeping it here for myself mostly, and if someone finds it useful, that's a bonus.

---

## What's in here

```
hypr/
├── hyprland.conf      # Main entry point, sources everything else
├── variables.conf     # Key definitions (mainMod, colors, etc.)
├── monitors.conf      # Monitor layout
├── input.conf         # Mouse, keyboard, touchpad settings
├── appearance.conf    # Gaps, borders, blur, rounding
├── keybinds.conf      # All keyboard shortcuts
└── autostart.conf     # Apps that launch on login
```

---

## Why ALT instead of Super

The Super key on my keyboard broke. So `$mainMod = ALT` in `variables.conf`. If your Super key works fine, just change it there.

---

## What it supports

- Workspace-based navigation
- Vim-style window movement (H/J/K/L)
- Screenshots with `grim` and `slurp` (saved to `~/Pictures/`, auto-copied to clipboard)
- Volume and brightness keys
- Waybar at the top

---

## Dependencies

Install these on Arch:

```bash
sudo pacman -S hyprland waybar wofi dunst grim slurp wl-clipboard \
  brightnessctl playerctl network-manager-applet blueman hyprlock \
  kitty dolphin
```

---

## Setup

```bash
git clone https://github.com/korelium-oss/hypr.git
cp -r hypr ~/.config/
hyprctl reload
```

---

## Screenshot shortcuts

| Print | Full screenshot |
| Shift + Print | Area screenshot (drag to select) |

---

## License

MIT License. See [LICENSE](LICENSE) for details.
