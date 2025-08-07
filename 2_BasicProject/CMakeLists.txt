# 0. Create the source and cmakefile
# 1. mkdir build && cd $_
# 2. cmake .. // Generete the build files / Configure the project
# 3. cmake --build .
# ./Executable

cmake_minimum_required(VERSION 3.28)

project(
    CppProjectTemplate
    VERSION 1.0.0
    LANGUAGES C CXX)

add_library(Library STATIC my_lib.cc)

add_executable(Executable main.cc)

target_link_libraries(Executable PUBLIC Library)
