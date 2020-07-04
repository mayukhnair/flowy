# Flowy
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) ![crates.io](https://img.shields.io/crates/v/flowy.svg) ![Build Flowy](https://github.com/vineetred/flowy/workflows/Build%20Flowy/badge.svg?branch=master)

## Demo
![](https://github.com/vineetred/flowy/blob/master/demo.gif)

## Usage
* You can either download the binary or get the Debian package.

### Binary - Recommended
* If you use the binary, just run it by typing ```flowy -d``` or ```flowy --dir``` to set the path to the wallpaper directory.

### Debian package
* If you use the Debian package, then it will install flowy as a ```systemd``` service. During installation, flowy will ask you your directory. 
* Once the installation is done, run the command ```systemctl --user start flowy.service``` to run the application.
* Once installation is done and you would still like to change the directory, go to the systemd service file found at ```/etc/systemd/user``` and change the directory in that file.

### Experimental
* By default, flowy evenly sets the wallpaper change time based on the number of wallpapers there are. In case you would like to modify these times, it can be done so by editing the ```times.toml``` file found in the ```/home``` directory. You need to comment the ```flowy::generate_config``` function call in ```main.rs``` and then build it after modifying the config file.

**TODO**
* GUI
* Match the stars given the location
