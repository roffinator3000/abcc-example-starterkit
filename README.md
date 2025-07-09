# abcc-example-starterkit
This is a stand-alone example application using the Anybus CompactCom Driver API ([abcc-api](https://github.com/hms-networks/abcc-driver-api)) ported for the [Anybus CompactCom Starter Kit](https://anybus.com/starterkit40) evaluation platform.
### Purpose
To enable easy evaluation and inspiration to [Anybus CompactCom](https://www.hms-networks.com/embedded-network-interfaces) prospects.

## Prerequisites
### System
- This example application shall be built for and ran in a Windows environment.
### Anybus Transport Provider
- The free Anybus Transport Provider DLL is required. [Download](https://hmsnetworks.blob.core.windows.net/nlw/docs/default-source/products/anybus/monitored/software/hms-anybus-transport-provider-1.zip?sfvrsn=e636aad6_44) and install this DLL.
### CMake
- If you do not yet have CMake, [download](https://cmake.org/download) and install it before continuing.
### Visual Studio
- In order to build this project you need the Build Tools for Visual Studio. They are included with Visual Studio (not in VS Code!), if you are using a different IDE you can [download](https://visualstudio.microsoft.com/downloads) and install them seperatly as well. 
### Git
- Of course, you will need to have Git installed. See [this tutorial](https://github.com/git-guides/install-git) on how to install Git.

## Cloning
### Flag? What flag?
This repository contain submodules [abcc-driver-api](https://github.com/hms-networks/abcc-api), [abcc-driver](https://github.com/hms-networks/abcc-driver) and [abcc-abp](https://github.com/hms-networks/abcc-abp) that must be initialized. Therefore, pass the flag `--recurse-submodules` when cloning.

```
git clone --recurse-submodules https://github.com/hms-networks/abcc-example-starterkit.git
```
#### (In case you missed it...)
If you did not pass the flag `--recurse-submodules` when cloning, the following command can be run:
```
git submodule update --init --recursive
```

## Build and run
### Step 1. CMake
This example application utilizes the Anybus CompactCom Driver API's CMake module file in a top level CMakelLists.txt file to generate a complete Visual Studio project.

To generate the project, open a terminal in Visual Studio or, if you are not using Visual Studio, select "Visual Studio Build Tools 20xx Release - x86" as compiler for CMake and let it reconfigure. Then open the "x64 Native Tools Command Prompt for VS" as the terminal and run the lines below, starting in the repository root.
```
mkdir build
```
```
cd build
```
```
cmake ..
```

### Step 2. Visual Studio
Open the generated project solution *.sln* file and run the Local Windows Debugger (green play button). The Project should build and run!
Without Visual Studio run "CMake Debug" or start the freshly generated .exe in the build directory manually.
#### (Nothing is happening...)
Make sure that your Starter Kit is powered on and the USB cable is plugged in. See the [Starter Kit Reference Guide](https://hmsnetworks.blob.core.windows.net/nlw/docs/default-source/products/anybus/manuals-and-guides---manuals/hms-hmsi-27-224.pdf?sfvrsn=8dfb9d6_20) for more details.

