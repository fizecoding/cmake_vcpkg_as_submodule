# Templet of cmake wiht vcpkg as submodule

- [中文](./readme_cn.md)

## requirement

- VSCode
  -C/C++ Extension Pack
- pkg-config
- git
- gcc & g++
- [vcpkg](https://github.com/microsoft/vcpkg)
- [more](https://github.com/microsoft/vcpkg#installing-linux-developer-tools)

## step

1. init git repository
2. use `git submodule add <url> <path>` to add vcpkg as submodule of the project.
3. switch to vcpkg path,run `bootstrap-vcpkg.sh`see at [Quick Start: Unix](https://github.com/microsoft/vcpkg#quick-start-unix)
4. pass `CMAKE_TOOLCHAIN_FILE` to CMakeLists.txt,see at [Vcpkg as a Submodule](https://github.com/microsoft/vcpkg#vcpkg-as-a-submodule)
5. enjoy

## notice

if you want to install new lib,just switch to vcpkg path and run`./vcpkg install` to install.
