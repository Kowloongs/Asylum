#
# Copyright (C) 356 - 999. Asytumn Technology Co., Ltd. All rights reserved.
#

cmake_minimum_required(VERSION 2.8.11)

project(Asylum)
include(CMakeToolsHelpers OPTIONAL)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set(_PROJECT_ROOT ${CMAKE_CURRENT_LIST_DIR} CACHE INTERNAL "Root" FORCE)

#
# Output paths.
#
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")

    option(compile_options_C "passes a string to the command line of the C compiler" OFF)
if(NOT "${compile_options_C}" STREQUAL "OFF")
    set(CMAKE_C_FLAGS "${compile_options_C} ${CMAKE_C_FLAGS}")
endif()
    option(compile_options_CXX "passes a string to the command line of the C++ compiler" OFF)
if(NOT "${compile_options_CXX}" STREQUAL "OFF")
    set(CMAKE_CXX_FLAGS "${compile_options_CXX} ${CMAKE_CXX_FLAGS}")
endif()

add_subdirectory(apr)


