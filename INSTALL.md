# 0 Greetings
Welcome to the installation!

**Contents**

  1. Requirements
  2. Installation
  3. Running
  4. Debugging

# 1 Requirements
You will need the following libraries, headers and tools:
  * at least g++ 4.8 or clang 3.3
  * boost
  * [cmake](http://www.cmake.org/)
  * [jack](https://github.com/jackaudio) (TODO: jack2 in the future?)

There are plugins that might require:
  * [zynaddsubfx](http://zynaddsubfx.sourceforge.net/), a version from at least April 2015 (TODO: make optional)
  * [sndfile](http://www.mega-nerd.com/libsndfile/)

# 2 Installation
The initial installation and updating are different processes.

For the initial installation, type in this directory:
```sh
git submodule init
git submodule update

mkdir build
cd build
# for a release build using clang (suggested), where /path/to/zynaddsubfx is
# the binary executable for zynaddsubfx
cmake	-DCOMPILER=clang \
	-DCMAKE_BUILD_TYPE=Release \
	-DZYN_BINARY=/path/to/zynaddsubfx \
	..
```

In order to update the code, go to the main directory and type
```sh
./update
```

# 3 Running
You can try this:
```sh
./src/core/minimal ./src/songs/libdemo.so
```

# 4 Debugging
TODO

