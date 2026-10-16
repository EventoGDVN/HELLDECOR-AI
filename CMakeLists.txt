
cmake_minimum_required(VERSION 3.21)

project(HELLDECOR_AI)

add_library(${PROJECT_NAME} SHARED
    main.cpp
)

if (NOT DEFINED ENV{GEODE_SDK})
    message(FATAL_ERROR "GEODE_SDK is not set")
endif()

include($ENV{GEODE_SDK}/CMakeLists.txt)

