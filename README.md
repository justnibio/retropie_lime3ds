# Lime3DS Setup for Retropie

This will add an entry on [Retropie-Setup](https://github.com/RetroPie/RetroPie-Setup) for [Lime3ds emulator](https://lime3ds.github.io/) running on a ARM64 (aka Raspberry) machine.

## Requirements

Check if you have 3DS already listed in file `~/RetroPie-Setup/platforms.cfg`.

If not, create (or edit) file `/opt/retropie/configs/all/platforms.cfg` and add:

```
switch_exts=".3ds"
switch_fullname="3DS"
```

## Install

After that, install the Lime3ds setup script with:

```bash
sudo apt install -y flatpak
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install -y flathub app.xemu.xemu
```

Now you can run **RetroPie Setup** script and `xemu` will available under `exp` (experimental) packages section.
