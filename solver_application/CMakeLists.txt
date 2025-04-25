cmake_minimum_required(VERSION 3.28.3)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(equation)

#add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib formatter_ex_lib)

#add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib solver_lib)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib)

add_executable(equation equation.cpp)

target_link_libraries(equation 
${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib/_build/libformatter_ex.a
${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib/_build/libformatter.a
${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib/_build/libsolver_lib.a)

