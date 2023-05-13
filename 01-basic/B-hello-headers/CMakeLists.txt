# Set the minimum version of CMake that can be used
# To find the cmake version run
# $ cmake --version
cmake_minimum_required(VERSION 3.5)

# Set the project name
project (hello_headers)

# Create a sources variable with a link to all cpp files to compile
set(SOURCES
    src/Hello.cpp
    src/main.cpp
)

# Add an executable with the above sources
add_executable(hello_headers ${SOURCES})

# Set the directories that should be included in the build command for this target
# when running g++ these will be included as -I/directory/path/
target_include_directories(hello_headers
    PRIVATE 
        ${PROJECT_SOURCE_DIR}/include
)

message(NOTICE "PROJECT_NAME = ${PROJECT_NAME}")
message(NOTICE "CMAKE_SOURCE_DIR = ${CMAKE_SOURCE_DIR}")
message(NOTICE "CMAKE_CURRENT_SOURCE_DIR = ${CMAKE_CURRENT_SOURCE_DIR}")
message(NOTICE "PROJECT_SOURCE_DIR = ${PROJECT_SOURCE_DIR}")
message(NOTICE "CMAKE_BINARY_DIR = ${CMAKE_BINARY_DIR}")
message(NOTICE "CMAKE_CURRENT_BINARY_DIR = ${CMAKE_CURRENT_BINARY_DIR}")
message(NOTICE "PROJECT_BINARY_DIR = ${PROJECT_BINARY_DIR}")