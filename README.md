# ZMK Config for M0nk's Wireless Corne

Custom ZMK configuration for wireless Corne keyboard.

## Layout Summary

### Layer 0 (QWERTY)
- Standard QWERTY layout
- Bottom corners: Both SHIFT keys
- Thumbs (L→R): Super, Layer1, Space | Enter, Layer2, Alt

### Layer 1 (LOWER - Numbers + Media)
**Left hand:**
- Q: Launch OBS (Super+O macro)
- 2-5: Numbers
- D: Volume Down
- F: Volume Up
- G: Launch Spotify (Super+S macro)
- C: Previous Track
- V: Next Track
- B: Play/Pause

**Right hand:**
- Numbers 6-0
- Arrow keys (left/down/up/right on J/K/L/;)

### Layer 2 (RAISE - Symbols)
- Symbols and brackets
- Standard symbol layer

### Layer 3 (ADJUST - Bluetooth)
- Bluetooth device selection (0-3)
- Bluetooth clear
- Bootloader mode

## Building Firmware

This repo uses GitHub Actions to build firmware automatically.

1. Push changes to GitHub
2. Go to Actions tab
3. Download the firmware `.uf2` files from the build artifacts

## Flashing

1. Connect keyboard via USB
2. Double-tap reset button to enter bootloader mode
3. Keyboard appears as USB drive
4. Drag & drop the `.uf2` file for that side
5. Keyboard automatically reboots with new firmware
6. Repeat for other half

## App Launcher Setup

The keyboard sends these key combos for app launching:
- **OBS**: Super+O
- **Spotify**: Super+S

Map these in GNOME Settings → Keyboard → Custom Shortcuts:
```bash
# Settings → Keyboard → View and Customize Shortcuts → Custom Shortcuts
Name: Launch OBS
Command: obs
Shortcut: Super+O

Name: Launch Spotify
Command: spotify
Shortcut: Super+S
```

## Notes

- Media keys (volume, play/pause, track skip) work natively
- Bluetooth can pair with up to 4 devices
- Battery lasts weeks on nice!nano with typical use
