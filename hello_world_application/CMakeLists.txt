cmake_minimum_required(VERSION 3.28.3)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(hello_world)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib)

add_executable(hello_world hello_world.cpp)

target_link_libraries(hello_world
${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib/_build/libformatter_ex.a
${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib/_build/libformatter.a)