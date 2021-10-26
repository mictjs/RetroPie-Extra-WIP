Focused on the latest version of Ubuntu

# RetroPie-Extra-WIP

This is a **collection of unofficial installation scripts for RetroPie** allowing you to quickly and easily **install emulators, ports and libretrocores** that haven't been included in RetroPie for one reason or another. These scripts can be considered experimental at best. 

Those in the `master` branch have been tested reasonably and should work well but may have some flaws as they haven't gone through the RetroPie's watchful eyes yet.

Pull requests and issue reports are accepted and encouraged as well as requests. Feel free to use the issue tracker to send me any personal requests for new scripts that you may have.

## Installation 

The following commands clone the repo to your Raspberry Pi and then run `install-scripts.sh` to install the scripts in the `master` branch directly to the proper directories in the `RetroPie-Setup/` folder.

```bash
cd ~
git clone https://github.com/mictjs/RetroPie-Extra-WIP.git
cd RetroPie-Extra-WIP/
./install-extras.sh
```
The installation script assumes that you are running it on a Raspberry Pi with the `RetroPie-Setup/` folder being stored in `/home/pi/RetroPie-Setup`. If your setup differs, just copy the scripts directly to the folder they need to be in.

## Usage

After installing **RetroPie-Extra**, the extra scripts will be installed directly in the **RetroPie Setup script** (generally in the experimental section), which you can run from either the command line or from the menu within Emulation Station.
```
cd ~
cd RetroPie-Setup/
sudo ./retropie_setup.sh
```

## Updating

The following commands update your Raspberry Pi to the latest repo and then run `install-scripts.sh` to install the scripts in the `master` branch directly to the proper directories in the `RetroPie-Setup/` folder.

```bash
cd ~
cd RetroPie-Extra/
git pull origin
./install-extras.sh
```

The installation script assumes that you are running it on a Raspberry Pi with the `RetroPie-Setup/` folder being stored in `/home/pi/RetroPie-Setup`. If your setup differs, just copy the scripts directly to the folder they need to be in.

## Troubleshooting

Here are some helpful hints for getting around some possible issues that you may encounter.

### The port I installed appears to close immediately upon launching.

In most cases, this is likely because the port requires external data files, especially in the case of game engines. In cases where shareware datafiles are available, the port will install them where possible. Otherwise, you will need to provide your own. The warning dialog box at the end of installation should usually tell you what files will be needed and where to place them. If you somehow don't see a dialog box after installation, you can open the script itself and look towards the bottom for the warning.

### What is the directory structure needed for lr-daphne?

I haven't worked that out yet. If you have, drop me a line.

## Included Software

### Master Branch

#### Emulators

- [X] - `gearboy.sh` - Gameboy emulator - **Tested and works well.**
- [X] - `pico8.sh` - Fantasy Game Emulator - Adds as a new system in RetroPie so you can directly launch carts.
- [X] - `pokemini.sh` - Pokemon Mini emulator - **Tested and works well.**

#### Libretrocores

- [X] - `lr-daphne.sh` - Daphne port to libretro - laserdisk arcade games.
- [X] - `lr-freej2me.sh` - A J2ME implementation for old JAVA phone games. **Tested and works.**
- [X] - `lr-mess-jaguar.sh` - Add support for using lr-mess for Jaguar games, uses atarijaguar system name to match lr-virtualjaguar.

#### Ports

- [X] - `chocolate-doom`.sh - DOOM source port - **Tested and works well.**
- [X] - `crispy-doom.sh` - DOOM source port - **Tested and works well.**
- [X] - `easyrpg-player.sh` - RPG Maker 2000/2003 interpreter - **Tested and works well.**
- [X] - `reminiscence.sh` - Flashback engine clone - **Tested and works well.**
- [X] - `sm64ex.sh` - Super Mario 64 PC Port for Pi4 - Works extremely well on Pi 4.
- [X] - `wizznic.sh` - Puzznic clone - **Tested and works well.**
- [X] - `zeldansq.sh` - Zelda: Navi's Quest fangame - **Tested and works well.**

#### Supplementary

- [X] - `fun-facts-splashscreens.sh` - Set up some loading splashscreens with fun facts.
- [X] - `joystick-selection.sh` - Set controllers for RetroArch players 1-4.
- [X] - `screenshot.sh` - Take screenshots remotely through SSH - **Tested and works well.**

### Future To-Do List 

I've moved this over to the [TODO.md](/TODO.md) file.

## Hall of Fame - Scripts accepted into RetroPie-Setup

- [X] - LXDE - LXDE Desktop.
- [X] - SimCoupe - Sam Coupe Emulator.
- [X] - Oricutron - Oric 1/Oric Atmos emulator.
- [X] - sdltrs - Radio Shack TRS-80 Model I/III/4/4P emulator.
- [X] - ti99sim - Texas Instruments 99A emulator.
