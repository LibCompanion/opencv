# opencvWinRT

WinRT/UWP compatible fork of OpenCV 3.2.0. The adjustments are necessary to build OpenCV for UWP apps and especially for the Microsoft HoloLens.

## Building opencvWinRT

Simply use cmake to generate a Visual Studio project:
```
cd "<build_dir>"
cmake -G "Visual Studio 14 2015" -DCMAKE_SYSTEM_NAME=WindowsStore -DCMAKE_SYSTEM_VERSION=10.0 -DCMAKE_CROSSCOMPILING=OFF "<src_dir>"
```

If you prefer the cmake-gui instead, make sure to add the following CMake flags before pressing *Configure* the first time:
```
CMAKE_SYSTEM_NAME = WindowsStore
CMAKE_SYSTEM_VERSION = 10.0
CMAKE_CROSSCOMPILING = OFF
```
Open the generated project file `OpenCV.sln` and build the `INSTALL` target.
