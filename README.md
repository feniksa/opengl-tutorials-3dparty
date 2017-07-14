# opengl-tutorials-3dparty
Build environment for opengl-tutorials repo

This repo contain pre-build

# List of compontets
* GLEW
* GLM
* SDL2
* SDL2_Image
* GTEST

# How to build/update rootfs (win64)

Schema of preparing rootfs are:
* All upacked packages, that are ready for build, will be at c:\distros directory
* Build will be done by Visual Studio 2015
* Install directory for rootfs will be c:\workspace\opengl-tutorials-3dparty\win64\rootfs

As all packages builded by Visual Studio, all commands must be run from Visual Studio Command Prompt.
To run it, start Visual Studio, at menu select: Tools -> Visual Studio Command Prompt

Specify CMAKE_PREFIX_PATH and CMAKE_LIBRARY_PATH to give cmake hint, where to find libraries

## GLEW
* Download GLEW: https://sourceforge.net/projects/glew/files/glew/2.0.0/glew-2.0.0-win32.zip/download
* GLEW already contain pre-build image, no need to build it
* Unpack GLEW to c:\workspace\opengl-tutorials-3dparty\win64\rootfs\GLEW-2.0.0

## GLM
* Download GLM: https://github.com/g-truc/glm/archive/0.9.8.4.zip
* Unpack GLM to c:\distros
* cd to glm directory
* Create build dir: mkdir build
* Configure:
  $ cmake -DCMAKE_BUILD_TYPE=release -DCMAKE_INSTALL_PREFIX="c:\workspace\opengl-tutorials-3dparty\win64\rootfs\GLM-0.9.8.4" -G "Visual Studio 14 2015 Win64" ..
* Open studio and run BUILD_ALL and INSTALL targets

## SDL2
* Download SDL2: https://www.libsdl.org/release/SDL2-2.0.5.zip
* Unpack to c:\distros
* cd to c:\distros\SDL2-2.0.5
* create build directory
* Configure: 
  $ cmake -DCMAKE_BUILD_TYPE=release -DCMAKE_INSTALL_PREFIX="c:\workspace\opengl-tutorials-3dparty\win64\rootfs\SDL2-2.0.5" -G "Visual Studio 14 2015 Win64" ..
* Open studio and run BUILD_ALL and INSTALL targets

# SDL2_Image
* Download SDL_image: https://www.libsdl.org/projects/SDL_image/release/SDL2_image-2.0.1-win32-x64.zip
* SDL2_Image already contain pre-build image, no need to build it
* Unpack GLEW to c:\workspace\opengl-tutorials-3dparty\win64\rootfs\SDL_image-2.0.1

# GTEST
* Download latest gtest
* Unpack it, create build directory
* Configure it with command:
$ cmake -DCMAKE_BUILD_TYPE=release -DCMAKE_INSTALL_PREFIX="c:\usr\lib\gtest-1.8.0" -G "Visual Studio 15 2017 Win64" ..
* Open studio and run BUILD_ALL and INSTALL targets