cmake_minimum_required(VERSION 3.15)
project(test)
# set(SRC add.cpp div.cpp mult.cpp sub.cpp main.cpp)
set(EXECUTABLE_OUTPUT_PATH ./bin/)
# aux_source_directory(${PROJECT_SOURCE_DIR}/src SRC)
file(GLOB SRC ${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp)
set(CMAKE_CXX_STANDARD 11)
include_directories(${PROJECT_SOURCE_DIR}/include)
add_executable(app ${SRC})