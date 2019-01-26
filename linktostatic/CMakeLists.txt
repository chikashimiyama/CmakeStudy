cmake_minimum_required(VERSION 3.5)

project(simplelib)

add_library(simplelib STATIC simple.cpp simple.h)

add_executable(simpleexec main.cpp)

target_link_libraries(simpleexec simplelib)