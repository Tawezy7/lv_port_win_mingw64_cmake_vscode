# pc_simulator_win_vscode

用于 LittlevGL 的 PC 模拟器项目在 VSCode 中使用

## 如何使用它：
###  教程
1) 下载并安装 [Git](https://git-scm.com/downloads) 和 CMake
2) 下载 [MinGW-W64](https://github.com/niXman/mingw-builds-binaries/releases/download/13.2.0-rt_v11-rev0/x86_64-13.2.0-release-posix-seh-ucrt-rt_v11-rev0.7z) 并解压至合适的地方
3) 克隆此存储库:
    - 打开命令提示符（Win 键 + R -> cmd -> Enter）或 PowerShell（Win 键 + R -> powershell -> Enter）或 Git bash（如果您想要与 C：/Users/username 不同的文件夹，则必须导航到它）并键入：`git clone --recurse-submodules https://github.com/Tawezy7/lv_port_win_mingw64_cmake_vscode.git`
5) 打开 VSCode 并根据建议安装 CMake 插件
6) 配置 CMake 工具包为下载好的编译器(将bin目录添加至系统环境变量后，再用CMake插件扫描工具包)
7) 在左下角找到 CMake 插件的编译按钮进行编译，编译完成然后运行
8) 如果一切顺利，您应该会看到您的模拟器正在运行。
