cmake_minimum_required(VERSION 3.5)

project(zad3)
file(GLOB SOURCES "src/*.cpp")
include_directories(include)
add_executable(myProgram ${SOURCES})

