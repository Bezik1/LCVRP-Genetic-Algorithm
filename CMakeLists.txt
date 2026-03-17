cmake_minimum_required(VERSION 3.16)
project(LCVRP-Genetic-Algorithm)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

if(APPLE)
    list(APPEND CMAKE_PREFIX_PATH "/opt/homebrew")
    set(CMAKE_INSTALL_RPATH_USE_LINK_PATH TRUE)
    list(APPEND CMAKE_INSTALL_RPATH "/opt/homebrew/lib")
endif()

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)

file(GLOB_RECURSE LIB_SOURCES "src/*.cpp")
list(REMOVE_ITEM LIB_SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp")

add_executable(main src/main.cpp ${LIB_SOURCES})