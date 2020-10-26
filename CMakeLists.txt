# CMakeList.txt : CMake project for BasicWindows001, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

project ("CppWinRTTemplate")

# Add source to this project's executable.
add_executable (${CMAKE_PROJECT_NAME} "main.cpp" "pch.h")
target_compile_features(${CMAKE_PROJECT_NAME} PRIVATE cxx_std_20)
target_precompile_headers(${CMAKE_PROJECT_NAME} PUBLIC pch.h)
