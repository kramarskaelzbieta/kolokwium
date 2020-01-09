cmake_minimum_required(VERSION 3.5)

project(kolokwium)
file(GLOB SOURCES "src/*.cpp")
include_directories(include)
add_executable(myProgram ${SOURCES})
install(TARGETS myProgram DESTINATION ~/Pulpit/kolokwium/bin)
