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
- [X] - `lr-freej2me.sh` - A J2ME implementation for old JAVA phone games.
- [X] - `lr-mess-jaguar.sh` - Add support for using lr-mess for Jaguar games, uses atarijaguar system name to match lr-virtualjaguar.

#### Ports

- [X] - `amphetamine.sh` - 2D Platforming Game - **Tested, runs well. Requires keyboard.**
- [X] - `barrage.sh` - Shooting Gallery action game - **Tested and works well, requires mouse.**
- [X] - `bermudasyndrome.sh` - Bermuda Syndrome engine - **Tested, runs, possibly instable.**
- [X] - `bloboats.sh` - Fun physics game - **Tested and works well, OpenGL game running through glshim.**
- [X] - `breaker.sh` - Arkanoid clone - **Tested and works well.**
- [X] - `burgerspace.sh` - BurgerTime clone - **Tested and works well.**
- [X] - `chocolate-doom`.sh - DOOM source port - **Tested and works well.**
- [X] - `chocolate-doom-system`.sh - For setting up DOOM as an emulated system, not port.
- [X] - `chromium.sh` - Open Source Web Browser - **Tested and works well.**
- [X] - `corsixth.sh` - Theme Hospital engine clone - **Tested and works well.**
- [X] - `crack-attack.sh` - Tetris Attack clone - **Tested and works well. Minor color issue needs to be fixed with glshim.**
- [X] - `crispy-doom.sh` - DOOM source port - **Tested and works well.**
- [X] - `crispy-doom-system.sh` - For setting up DOOM as an emulated system, not port.
- [X] - `deadbeef.sh` - Music and ripped game music player - **Tested and works well.**
- [X] - `devilutionx.sh` - Diablo source port - **Tested and working well on Pi4.**
- [X] - `easyrpgplayer.sh` - RPG Maker 2000/2003 interpreter - **Tested and works well.**
- [X] - `freeciv.sh` - Civilization online clone - **Tested and works well, I may soon replace it to compile latest freeciv so that players can play with newer clients.**
- [X] - `freedink.sh` - Dink Smallwood engine - **Tested and works well.**
- [X] - `freesynd.sh` - Syndicate clone - **Tested and has occasional crash issues. Save between levels to avoid losing progress.**
- [X] - `gamemaker.sh` - Install the 3 gamemaker games - **Tested and works well.**
- [X] - `ganbare.sh` - Japanese 2D Platformer - **Tested and works well, does not require Japanese to play.**
- [X] - `hcl.sh` - Hydra Castle Labrinth - **Tested and works well.**
- [X] - `heboris.sh` - Tetris The Grand Master clone - **Tested and works well.  To fix sound, change settings from MIDI to MP3.**
- [X] - `hurrican.sh` - Turrican clone. - **Tested and works well, minor graphics issues.**
- [X] - `iceweasel.sh` - Rebranded Firefox Web Browser - **Tested and works well.**
- [X] - `kaiten-patissier-cs.sh` - Japanese 2D Platformer - **Tested and works well, has English mode.**
- [X] - `kaiten-patissier-ura.sh` - Japanese 2D Platformer - **Tested and works well, has English mode.**
- [X] - `kaiten-patissier.sh` - Japanese 2D Platformer - **Tested and works well, has English mode.**
- [X] - `kodi-extra.sh` - Kodi Media Player 16 with controller support as a separate system - **Tested and works well.**
- [X] - `kweb.sh` - Minimal kiosk web browser - **Tested and working well generally. Media may not be working well, I need to understand it better first to say.**
- [X] - `lbreakout2.sh` - Open Source Breakout game - **Tested and working well, requires mouse.**
- [X] - `lgeneral.sh` - Open Source strategy game - **Tested and working well, requires mouse.**
- [X] - `lmarbles.sh` - Open Source Atomix game - **Tested and working well, requires mouse.**
- [X] - `ltris.sh` - Open Source Tetris game - **Tested and working well, requires keyboard.**
- [X] - `manaplus.sh` - 2D MMORPG client - **Tested and works well, requires mouse.**
- [X] - `netsurf.sh` - Lightweight web browser - **Tested and works well.**
- [X] - `nkaruga.sh` - Ikaruga demake. **Tested and works well, requires keyboard.**
- [X] - `nxengine.sh` - The standalone version of the open-source clone/rewrite of Cave Story - **Tested and works well.**
- [X] - `openjazz.sh` - Jazz Jackrabbit source port.
- [X] - `pingus.sh` - Lemmings clone - **Tested and works well, requires mouse.**
- [X] - `prboom-plus.sh` - Enhanced DOOM source port - lightly **tested, seems to work.**
- [X] - `rawgl.sh` - Another World source port - **Tested, occasionally crashes when button held when switching scenes?**
- [X] - `reminiscence.sh` - Flashback engine clone - **Tested and works well. **
- [X] - `retrobattle.sh` - Fun retro style platform game - **Tested and works well.**
- [X] - `rickyd.sh` - Rick Dangerous clone - **Tested and works well, requires keyboard.**
- [X] - `rockbot.sh` - Mega Man clone. **Tested and screen flickers like crazy until proper settings are applied. Check package help for more info.**
- [X] - `rott-darkwar.sh` - Rise of the Triad source port with joystick support - **Tested and works well.**
- [X] - `rott-huntbgin.sh` - Rise of the Triad (shareware version) source port with joystick support.
- [X] - `sdl-bomber.sh` - Simple Bomberman clone - **Tested and works well, turn down the volume perhaps. **
- [X] - `shiromino.sh` - Tetris the Grand Master Clone - Requires keyboard to restart/quit.
- [X] - `sorr.sh` - Streets of Rage Remake port - **Tested and works well. Use fullscreen fast video mode.**
- [X] - `sm64ex.sh` - Super Mario 64 PC Port for Pi4 - Works extremely well on Pi 4.
- [X] - `texmaster2009.sh` - Tetris TGM clone - **Tested and works well. Works on Pi4.**
- [X] - `tinyfugue.sh` - MUD client - **Tested and works well.**
- [X] - `ulmos-adventure.sh` - Simple Adventure Game - **Tested and works well.**
- [X] - `vgmplay.sh` - Music Player - **Tested and works well. Plays .vgm and .vgz game music rips. Command line client only.**
- [X] - `vorton.sh` - Highway Encounter Remake in Spanish - **Tested and works well.**
- [X] - `warmux.sh` - Worms Clone - **Tested and works well. Possible issues with config files in wrong places?**
- [X] - `weechat.sh` - Console IRC Client - **Tested and works well.**
- [X] - `wizznic.sh` - Puzznic clone - **Tested and works well.**
- [X] - `xash3d-fwgs.sh` - Half-Life engine source port.
- [X] - `zeldansq.sh` - Zelda: Navi's Quest fangame - **Tested and works well.**
- [X] - `zeldapicross.sh` - Zelda themed Picross fangame - **Tested and works well, may require keyboard.**

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

## Contact Info / Additional Information

- **Twitter**: [@zerojay](https://twitter.com/zerojay) - Often posting new information and additions from the repository to the #retropie hashtag.  
- **IRC**: zerojay on irc.freenode.net, #retropie/#retropie-extra.

If you wish to be up-to-date about all the changes happening to the repository as they happen, feel free to join the #retropie-extra channel on **Freenode**.
