cmake_minimum_required(VERSION 3.15)
project(test)
# set(SRC add.cpp div.cpp mult.cpp sub.cpp main.cpp)
set(EXECUTABLE_OUTPUT_PATH ./bin/)
# aux_source_directory(${PROJECT_SOURCE_DIR}/src SRC)
file(GLOB SRC ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)              #所用到的源文件只有main.cpp一个
set(CMAKE_CXX_STANDARD 11)
include_directories(${PROJECT_SOURCE_DIR}/include)    
# add_executable(app ${SRC})
# add_library(calc SHARED ${SRC})
# set(LIBRARY_OUTPUT_PATH ${CMAKE_CURRENT_SOURCE_DIR})   #不再需要指定库文件输出目录
# add_library(calc SHARED ${SRC})  #不再需要

# 需要生成可执行文件
# 需要链接库文件
link_directories(${PROJECT_SOURCE_DIR}/lib1)
link_libraries(calc)
add_executable(app ${SRC})  