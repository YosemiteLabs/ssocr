cmake_minimum_required(VERSION 3.1.0)

project(ssocr C)

set (CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/CMakeModules)

find_package(Imlib2)

FILE(GLOB sources *.c)

#ADD_LIBRARY(libssocr ${sources})
#TARGET_LINK_LIBRARIES(libssocr)
add_executable(ssocr ${sources})
target_include_directories(ssocr PRIVATE /usr/local/include /opt/X11/include)
target_link_libraries(ssocr PRIVATE ${IMLIB2_LIBRARIES})
