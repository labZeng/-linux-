# 指定CMake最低版本要求
cmake_minimum_required(VERSION 3.10.2)

# 定义项目名称为test_monitor，使用C++语言
project(test_monitor LANGUAGES CXX)

# 设置CMake模块查找路径，用于查找自定义cmake模块
set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake")

# 设置C++标准为C++17
set(CMAKE_CXX_STANDARD 17)

# 添加各个子模块目录
# RPC管理模块
add_subdirectory(rpc_manager)

# 系统监控测试模块
add_subdirectory(test_monitor)

# Protocol Buffers定义模块
add_subdirectory(proto)

# 显示监控GUI模块
add_subdirectory(display_monitor)