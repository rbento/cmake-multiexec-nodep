﻿cmake_minimum_required (VERSION 3.18)

project ("project-name")

set(C_STANDARD 99) # Supported values are 90, 99 and 11.
set(C_STANDARD_REQUIRED ON)

add_definitions(-D_CRT_SECURE_NO_WARNINGS)

file(GLOB SOURCE_FILES *.c)

foreach(SOURCE_PATH ${SOURCE_FILES})

    get_filename_component(EXECUTABLE_NAME ${SOURCE_PATH} NAME_WE)

    add_executable(${EXECUTABLE_NAME} ${SOURCE_PATH})

endforeach(SOURCE_PATH ${SOURCE_FILES})
