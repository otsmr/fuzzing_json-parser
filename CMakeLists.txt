cmake_minimum_required(VERSION 3.10)  
project(json_parser)

add_library(json_parser STATIC json.c)

target_include_directories(json_parser PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})