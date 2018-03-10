# opencvWinRT

WinRT/UWP compatible fork of OpenCV 3.2.0. The adjustments are necessary to build OpenCV for UWP apps and especially for the Microsoft HoloLens.

## Building opencvWinRT

Simply use CMake to generate a Visual Studio project:
```
cd "<build_dir>"
cmake -G "Visual Studio 15 2017" -DCMAKE_SYSTEM_NAME=WindowsStore -DCMAKE_SYSTEM_VERSION=10.0 -DCMAKE_CROSSCOMPILING=OFF "<src_dir>"
```

If you prefer the CMake GUI instead, make sure to add the following CMake variables before pressing *Configure* the first time:
```
CMAKE_SYSTEM_NAME = WindowsStore
CMAKE_SYSTEM_VERSION = 10.0
CMAKE_CROSSCOMPILING = OFF
```
Open the generated project file `OpenCV.sln` and build the `INSTALL` target.
