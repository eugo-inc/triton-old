cmake_minimum_required(VERSION 3.13)

project(f2reduce LANGUAGES CXX)

add_library(f2reduce_plugin STATIC plugin.cpp)

target_include_directories(f2reduce_plugin PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_compile_features(f2reduce_plugin PUBLIC cxx_std_17)
