# 0. Create the source and cmakefile
# 1. mkdir build && cd $_
# 2. cmake .. // Generete the build files / Configure the project
# 3. cmake --build .
# ./Executable

cmake_minimum_required(VERSION 3.28)

project( CppProjectTemplate VERSION 1.0.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD          17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS       OFF)

set(LIBRARY_NAME Library)
set(EXECUTABLE_NAME Executable)

option(COMPILE_EXECUTABLE "Whether to compile the executable" OFF)

add_subdirectory(src)
if(COMPILE_EXECUTABLE)
    add_subdirectory(app)
endif()
