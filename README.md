# Steam CLI Launcher (Linux)

### 🌍 Read this in:
- [Português brasileiro](README.pt-BR.md)

A simple Python script to list installed Steam games on Linux and launch them directly from the terminal.

No opening Steam, no hunting for games with the mouse, no wasted time.

## Features

- Lists installed Steam games  
- Sorts games alphabetically  
- Launches the selected game via `steam://rungameid`  
- Automatically ignores Steam Linux Runtimes  
- Runs directly in the terminal  

> Note: Proton versions installed by Steam **appear in the list**, since they are also registered as apps. Steam runtimes are manually filtered out in the script.

## Project structure

```text
steam-cli-launcher/
├── steam-games        # main script (executable, no extension)
├── steam-games.py     # testing / development version
```

- steam-games is the file intended for daily use

- steam-games.py is only for testing and code adjustments

## Requirements
- Linux

- Steam installed

- Python 3

- `vdf` library

## Installing the dependency

```bash
pip install vdf
```

Or, depending on your distro:

```bash
sudo pacman -S python-vdf
```

## Installation
Give execution permission:

```bash
chmod +x steam-games
```

In my case, I placed the file in:

```text
~/.local/bin/
```

This way, the script can be executed from anywhere in the terminal, as long as `~/.local/bin/` is in your `PATH`.

## Usage
Just run:

```bash
steam-games
```

The script will list installed games.
Type the number corresponding to the game and it will be launched automatically via Steam.

## Notes
- Tested on Fedora KDE (Linux)

- Only locally installed games appear

- Proton versions installed by Steam appear in the list

- Steam Linux Runtimes are ignored
