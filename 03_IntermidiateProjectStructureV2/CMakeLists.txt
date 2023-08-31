cmake_minimum_required(VERSION 3.22)

project(
    CppProjectTemplate
    VERSION 1.0.0
    LANGUAGES C CXX
)

add_library(Library STATIC 
    src/my_lib.cc
)

target_include_directories(Library PUBLIC includes)

add_executable(Executable main.cc)

target_link_libraries(Executable PUBLIC Library)