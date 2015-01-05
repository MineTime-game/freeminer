# MineTime

[![Build Status](https://travis-ci.org/MineTime-game/MineTime-evo.png)](https://travis-ci.org/MineTime-game/MineTime-evo)

MineTime is an open source sandbox game.

MineTime is based on Freeminer which is developed by a [number of contributors](https://github.com/freeminer/freeminer/graphs/contributors) from all over the globe.

It aims to make the game fun while trading off some bits of perfectionism.

## Further documentation

## Default controls
- `WASD`: move
- `Space`: jump/climb
- `Shift`: sneak/go down
- `Q`: drop item
- `I`: inventory
- Mouse: turn/look
- Mouse left: dig/punch
- Mouse right: place/use
- Mouse wheel: select item
- `Esc`: pause menu
- `T`: chat
- `Z`: zoom
- `Tab`: player list

## Compiling
Install dependencies. Here's an example for

Debian/Ubuntu:
```bash
sudo apt-get install build-essential libirrlicht-dev cmake libbz2-dev \
libpng12-dev libjpeg8-dev libfreetype6-dev libxxf86vm-dev libgl1-mesa-dev \
libsqlite3-dev libvorbis-dev libopenal-dev libcurl4-openssl-dev libluajit-5.1-dev \
libleveldb-dev libsnappy-dev libgettextpo0 libmsgpack-dev
# optional:
sudo apt-get install libhiredis-dev cmake-curses-gui
```
___
Fedora:
```bash
# the first five is the closest to Debian/Ubuntu build-essential
sudo yum install make automake gcc gcc-c++ kernel-devel cmake irrlicht-devel \
bzip2-devel libpng-devel libjpeg-turbo-devel freetype-devel libXxf86vm-devel \
mesa-libGL-devel sqlite-devel libvorbis-devel openal-soft-devel libcurl-devel \
luajit-devel leveldb-devel snappy-devel gettext-devel msgpack msgpack-devel
```
___
Arch Linux:
```bash
sudo pacman -S curl irrlicht leveldb libvorbis luajit openal sqlite cmake
# From AUR
yaourt -S msgpack
```
<sup>Recommended irrlicht version: `1.8.1`</sup>

Download source code:
```bash
git clone --recursive https://github.com/minetime-game/minetime-evo.git
cd MineTime-evo
```

<sup>Recommended minimum compiler version: `gcc 4.8` or `clang 3.3`</sup>

Build it:
```bash
mkdir _build && cd _build
cmake ..
time nice make -j $(nproc || sysctl -n hw.ncpu || echo 2)
```

Play it!
```
cd ..
./bin/minetime
```
