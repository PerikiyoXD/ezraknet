# ezraknet
Stripped-down RakNet library specifically built for CMake.

(Original project: https://github.com/OculusVR/RakNet)

## Why?
Because RakNet contains unneeded files in it's official repository, and it's pretty annoying searching and building the specific stuff you need and not finish building examples or other subprojects. 

Here instead we have an straightforward generation. No samples, no shit. Just what you need.
And it works with CMake.

## How?
### Linux 
```
git clone https://github.com/PerikiyoXD/ezraknet
cd ezraknet
mkdir build
cd build
cmake .. -G"Unix Makefiles"
make
```

### MSYS2
```sh
git clone https://github.com/PerikiyoXD/ezraknet
cd ezraknet
mkdir build
cd build
cmake .. -G"MSYS Makefiles"
make
```
### Visual Studio 2017
```
git clone https://github.com/PerikiyoXD/ezraknet
cd ezraknet
mkdir build
cd build
cmake .. -G"Visual Studio 15 2017"
```
And open Visual Studio Solution (.sln) located inside ``build`` folder. (ie: C:/base/folder/ezraknet/build/ezraknet.sln)
