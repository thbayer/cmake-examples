# Set the minimum version of CMake that can be used
# To find the cmake version run
# $ cmake --version
cmake_minimum_required(VERSION 3.5)

set(CMAKE_BUILD_TYPE "RELEASE")

message(NOTICE "CMAKE_GENERATOR = ${CMAKE_GENERATOR}")
message(NOTICE "CMAKE_BUILD_TYPE = ${CMAKE_BUILD_TYPE}")
message(NOTICE "CMAKE_BINARY_DIR = ${CMAKE_BINARY_DIR}")
message(NOTICE "CMAKE_SOURCE_DIR = ${CMAKE_SOURCE_DIR}")


# Set the project name
project (hello_cmake)

# Add an executable
add_executable(hello_cmake main.cpp)
