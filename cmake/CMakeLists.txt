cmake_minimum_required(VERSION 3.27.4)
project(HexGen VERSION 1.0)

set(SOURCES
    ../src/Main.cpp
    ../src/HexGen.cpp
    ../src/HexGen.h
    ../src/Initialization.h
    ../src/Mesh.cpp
    ../src/Mesh.h
    ../src/StaticVars.h
)

add_executable(HexGen ${SOURCES})

if (CMAKE_GENERATOR MATCHES "Visual Studio")
    set_property(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT HexGen)
endif()