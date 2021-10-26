Focused on the latest versions of Ubuntu

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
cd RetroPie-Extra-WIP/
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
- [X] - `supermodel.sh` - Arcade Sega Model 3 emulator - **Tested and works well.**

#### Libretrocores

- [X] - `lr-2048.sh` - 2048 engine - 2048 port for libretro. - **Tested and works well.**
- [X] - `lr-bk.sh` - Elektronika БК-0010/0011/Terak 8510a emulator - BK port for libretro. - **Tested and works.**
- [X] - `lr-blastem.sh` - yet another Sega Genesis/Megadrive emulator - BlastEm port for libretro. - **Tested and works.**
- [X] - `lr-boom3.sh` - Doom 3 engine - dhewm3 port for libretro - **Tested and works (only for x86_64).**
- [X] - `lr-canary.sh` - 3DS emulator - Citra Canary for libretro. - Experimental (only for x86_64).
- [X] - `lr-cannonball.sh` - An Enhanced OutRun engine for libretro. - **Tested and works well.**
- [X] - `lr-chailove.sh` - 2D Game Framework with ChaiScript roughly inspired by the LÖVE API to libretro. - **Tested and works well.**
- [X] - `lr-citra.sh` - 3DS emulator - Citra for libretro. **Tested and works (only for x86_64).**
- [X] - `lr-craft.sh` - Minecraft engine - Craft port for libretro. - **Tested and works well.**
- [X] - `lr-crocods.sh` - Amstrad CPC emu - CrocoDS port for libretro. - **Tested and works.**
- [X] - `lr-daphne.sh` - Arcade LaserDisc - Daphne port to libretro. - Not Works :(
- [X] - `lr-easyrpg.sh` - RPG Maker 2000/2003 engine - EasyRPG Player interpreter port for libretro. - **Tested and works well.**
- [X] - `lr-ecwolf.sh` - Wolfestein 3D engine - ECWolf port based of Wolf4SDL for libretro. - **Tested and works well (only for x86_64).**
- [X] - `lr-freej2me.sh` - A J2ME implementation for old JAVA phone games. **Tested and works.**
- [X] - `lr-gearboy.sh` - Yet another Game Boy (Color) emulator - Gearboy port for libretro. - **Tested and works well.**
- [X] - `lr-gearcoleco.sh` - ColecoVision emulator - GearColeco port for libretro. - **Tested and works well.**
- [X] - `lr-lutro.sh` - Lua engine - lua game framework (WIP) for libretro following the LÖVE API. - **Tested and works well.**
- [X] - `lr-melonds.sh` - NDS emu - MelonDS port for libretro. - Tested and works.
- [X] - `lr-mesen-s.sh` - Yet another Super Nintendo emulator - Mesen-S port for libretro. - **Tested and works well (only for x86_64).**
- [X] - `lr-minivmac.sh` - Macintosh Plus Emulator - Mini vMac port for libretro. - Tested and works... sorta :\
- [X] - `lr-mu.sh` - Palm OS emu - Mu port for libretro. - **Tested and works.**
- [X] - `lr-oberon.sh` - Oberon RISC machine emulator for libretro. - It works.
- [X] - `lr-openlara.sh` - Tomb Raider engine - OpenLara port for libretro. - **Tested and works well.**
- [X] - `lr-play.sh` - PlayStation 2 emulator - Play port for libretro. - Experimental (only for x86_64)
- [X] - `lr-potator.sh` - Watara Supervision emulator based on Normmatt version - Potator port for libretro. - **Tested and works well.**
- [X] - `lr-race.sh` - Yet another Neo Geo Pocket (Color) emulator - RACE-NGPC-Emulator-PSP port for libretro.. - **Tested and works well.**
- [X] - `lr-reminiscence.sh` - Flashback engine - Gregory Montoir’s Flashback emulator port for libretro. - Tested and works.
- [X] - `lr-sameboy.sh` - Yet another Game Boy (Color) emulator - SameBoy Port for libretro. - **Tested and works well.**
- [X] - `lr-simcoupe.sh` - SAM Coupe emulator - SimCoupe port for libretro. - **Tested and works well.**
- [X] - `lr-thepowdertoy.sh` - Sandbox physics game for libretro. - **Tested and works well.**
- [X] - `lr-uzem.sh` - Uzebox engine - Uzem port for libretro. - **Tested and works well.**
- [X] - `lr-vemulator.sh` - SEGA Visual Memory Unit emulator - VeMUlator port for libretro. - **Tested and works well.**
- [X] - `lr-vitaquake2.sh` - Quake 2 engine - vitaQuake II port for libretro. - **Tested and works (MODS crash after game presentation video).**
- [X] - `lr-vitaquake3.sh` - Quake 3 engine - vitaQuake III port for libretro. - **Tested and works.**
- [X] - `lr-vitavoyager.sh` - Star Trek Voyager Elite Force Holomatch engine - Lilium Voyager (fork of ioquake3) port for libretro. - It loads, but, with Black Screen.


#### Ports

- [X] - `chocolate-doom`.sh - DOOM source port - **Tested and works well.**
- [X] - `crispy-doom.sh` - DOOM source port - **Tested and works well.**
- [X] - `easyrpg-player.sh` - RPG Maker 2000/2003 interpreter - **Tested and works well.**
- [X] - `reminiscence.sh` - Flashback engine clone - **Tested and works well.**
- [X] - `sm64ex.sh` - Super Mario 64 PC Port for Pi4 - Works extremely well on Pi 4.
- [X] - `wizznic.sh` - Puzznic clone - **Tested and works well.**
- [X] - `zeldansq.sh` - Zelda: Navi's Quest fangame - **Tested and works well.**

#### Supplementary

- [X] - `mame-tools` - This package provides tools to be used with MAME or to be used with other emulators, like CHDMAN tools that is a CD/AVI converter to CHD format. - **Tested and works well.**

### Future To-Do List 

I've moved this over to the [TODO.md](/TODO.md) file.

## Hall of Fame - Scripts accepted into RetroPie-Setup

- [X] - LXDE - LXDE Desktop.
- [X] - SimCoupe - Sam Coupe Emulator.
- [X] - Oricutron - Oric 1/Oric Atmos emulator.
- [X] - sdltrs - Radio Shack TRS-80 Model I/III/4/4P emulator.
- [X] - ti99sim - Texas Instruments 99A emulator.
