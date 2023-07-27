#使用 vcpkg 作为子模块的 cmake 模板

## requirement

- VSCode
  -C/C++ Extension Pack
- pkg-config
- gcc & g++
- [vcpkg](https://github.com/microsoft/vcpkg)
- [更多](https://github.com/microsoft/vcpkg#installing-linux-developer-tools)

## step

1. 初始化 git 仓库
2. 使用`git submodule add <url> <path>`添加 vcpkg 作为子模块。
3. 切换到 vcpkg 目录，运行`bootstrap-vcpkg.sh`参见[Quick Start: Unix](https://github.com/microsoft/vcpkg#quick-start-unix)
4. 在 CMakeLists.txt 中传入 CMAKE_TOOLCHAIN_FILE，参见[Vcpkg as a Submodule](https://github.com/microsoft/vcpkg#vcpkg-as-a-submodule)
5. enjoy

## notice

如果需要安装库，只需要切换到 vcpkg 目录，使用`./vcpkg install` 来安装新的库即可。
