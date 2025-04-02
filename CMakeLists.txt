cmake_minimum_required(VERSION 4.0)

project(imgui)

################################################################################
#                               CMake Setting
################################################################################

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

################################################################################
#                               Static Library 
################################################################################

file(GLOB_RECURSE SOURCE src/*.cpp)

add_library(imgui STATIC ${SOURCE})

target_include_directories(imgui PUBLIC
  include
)
