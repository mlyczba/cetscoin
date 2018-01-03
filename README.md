# CETScoin

**CETS** stands for: Cryptocurrency Exchange Trading System. 

It is an attempt to extend the LETSystem for community-based mutual aid networks
in which people exchange all kinds of goods and services with one another, without the need for money.

Like other cryptocurrencies, CETScoin is generated by mining it. This is a new component within such trading systems. Anyone with a computer system in the trading network is a potential miner. This role needs to be somehow 
incorporated into the exchange of goods.

Total available coins is: 18.446.744. Each block is mined every 2 minutes.

The best way to install CETScoin wallet is to compile it.


## Building CETScoin 

### General dependencies

Dependencies: GCC 4.7.3 or later, CMake 2.8.6 or later, and Boost 1.55.

You may download them from:

* http://gcc.gnu.org/
* http://www.cmake.org/
* http://www.boost.org/

## Linux


Get the tools needed:

GCC (min. 4.7.3)
```
sudo apt-get install gcc
```

Cmake (min. 2.8.6)
```
sudo apt-get install cmake
```

Boost: (1.55)
```
sudo apt-get install libboost1.55-all-dev
```

Run `make` command inside the `src/` directory.

To build, change to a directory where this file is located, and run `make`. The resulting executables can be found in `build/release/src`.

## Windows (64-bit)

**Visual C++ 2015 Build Tools**

http://landinghub.visualstudio.com/visual-cpp-build-tools

**Boost 1.60 libraries** 

https://sourceforge.net/projects/boost/files/boost-binaries/

Checked file: https://sourceforge.net/projects/boost/files/boost-binaries/1.60.0/boost_1_60_0-msvc-14.0-64.exe/download

**Install CMake**

https://cmake.org/download/

Checked file: https://cmake.org/files/v3.10/cmake-3.10.1-win64-x64.msi

**Install Python**

https://www.python.org/downloads/windows/

Checked file: https://www.python.org/ftp/python/3.6.4/python-3.6.4-amd64.exe

**Instructions:**

Start VS2015 x64 native Tools Command Prompt (As Administrator)

```
SETX BOOST_ROOT "C:\local\boost_1_60_0" /M
SETX BOOST_LIBRARYDIR "C:\local\boost_1_60_0\lib64-msvc-14.0" /M
cd src
mkdir build
cd build
cmake -G "Visual Studio 14 2015 Win64" ..
MSBuild CryptoNote.sln /p:Configuration=release /m
```
The executables will be build inside:
```cetscoin\build\src\Release```

## Mac - OSX

Use brew to install the dependencies:
```
brew install cmake
brew install boost
```

Run `make` command inside the `src/` directory. The resulting executables can be found in `build/release/src`.
