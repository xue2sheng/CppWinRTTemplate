﻿cmake_minimum_required (VERSION 3.8)

project ("CppWinRTTemplate")

set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} /SUBSYSTEM:WINDOWS")
add_executable (${CMAKE_PROJECT_NAME} "main.cpp" "pch.h")
target_precompile_headers(${CMAKE_PROJECT_NAME} PUBLIC pch.h)
target_compile_features(${CMAKE_PROJECT_NAME} PRIVATE cxx_std_20)
target_link_libraries(${CMAKE_PROJECT_NAME} WindowsApp)
