cmake_minimum_required(VERSION 2.8)     #最低cmake版本
project(hello_world)    #工程名称

SET(CMAKE_BUILD_TYPE Release)   #可编译方式 Release，该模式对应的模式为debug。后者是调试模式，系统运行会慢很多。所以要求有比较高效的运行方式，建议选择Release

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)   #设置可执行文件保存路径
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)      #设置链接库保存路径

include_directories(
${PROJECT_SOURCE_DIR}/include   #设置头文件目录
)

add_executable(hello_world src/hello_world.cpp src/main.cpp)    #选择需要编译的源文件
