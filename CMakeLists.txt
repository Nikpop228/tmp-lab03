cmake_minimum_required(VERSION 3.28.3)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(apps)

add_subdirectory(formatter_lib)

add_subdirectory(formatter_ex_lib)

add_subdirectory(solver_lib)

add_subdirectory(hello_world_application)

add_subdirectory(solver_application)