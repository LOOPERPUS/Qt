cmake_minimum_required(VERSION 3.8)

project(gvisual LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)

set ("${PROJECT_NAME}_BINARY_DIR" ${CMAKE_SOURCE_DIR}/bin)
set ("${PROJECT_NAME}_SOURCE_DIR" ${CMAKE_SOURCE_DIR}/src)
set ("${PROJECT_NAME}_LIB_DIR" ${CMAKE_SOURCE_DIR}/lib)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${${PROJECT_NAME}_BINARY_DIR})

if(MINGW)
set (CMAKE_PREFIX_PATH "D:\\Soft\\Programming\\Qt\\5.12.6\\mingw73_64\\")
endif()

if(MSVC)
set (CMAKE_PREFIX_PATH "D:\\Soft\\Programming\\Qt\\5.12.6\\msvc2017_64\\")
endif()

find_package(Qt5 COMPONENTS Widgets REQUIRED)
find_package(Qt5 COMPONENTS Core REQUIRED)
find_package(Qt5 COMPONENTS Gui REQUIRED)

add_subdirectory(src)