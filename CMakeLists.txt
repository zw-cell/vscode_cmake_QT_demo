cmake_minimum_required(VERSION 3.0.0)
project(textFinder VERSION 0.1.0 LANGUAGES C CXX)
# QT相关
set(CMAKE_AUTOMOC ON) # CMAKE_AUTOMOC:负责处理信号槽，生成信号的moc_xxx.cpp文件
set(CMAKE_AUTORCC ON) # CMAKE_AUTORCC: 负责处理qrc资源文件
set(CMAKE_AUTOUIC ON) # CMAKE_AUTOUIC: 负责处理ui文件，生成对应的ui_xxxx.h文件
set(CMAKE_CXX_STANDARD 17) # C++17
set(CMAKE_CXX_STANDARD_REQUIRED ON) # CMAKE_CXX_STANDARD_REQUIRED:指示构建系统是否要求使用所选择的C++标准
set(CMAKE_EXPORT_COMPILE_COMMANDS ON) # 会在构建过程中生成名为 compile_commands.json 的文件，其中包含了用于编译每个源文件的详细编译命令
set(QT6_PATH "/Users/zhengwang/QT/6.6.2/macos/lib/cmake") 
set(PROJECT_RESOURCE ${PROJECT_SOURCE_DIR}/resources/res.qrc)
set(CMAKE_PREFIX_PATH ${QT6_PATH}) # 告诉 CMake 在查找依赖项时应该搜索的路径
find_package(Qt6 REQUIRED COMPONENTS Widgets)
qt_standard_project_setup() # 项目范围默认标准设置
add_subdirectory(src/app)
add_subdirectory(src/MainWindow)
