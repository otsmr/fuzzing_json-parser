cmake_minimum_required(VERSION 3.10)  
project(json_parser)

add_library(json_parser STATIC json.c)

find_program(AFL_C_COMPILER afl-clang-fast)
find_program(AFL_CXX_COMPILER afl-clang-fast++)

set(CMAKE_C_COMPILER ${AFL_C_COMPILER})
set(CMAKE_CXX_COMPILER ${AFL_CXX_COMPILER})

target_include_directories(json_parser PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})