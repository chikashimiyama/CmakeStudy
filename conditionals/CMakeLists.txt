cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

project(conditional)

set(LIBRARY OFF)

if(LIBRARY)
	add_library(simplelib STATIC simple.cpp simple.h)
	add_executable(simpleexec main.cpp)
	target_link_libraries(simpleexec simplelib)
else()
	add_executable(simpleexec main.cpp simple.cpp simple.h)
endif()

