cmake_minimum_required(VERSION 3.10)
if(APPLE)
	find_library(COCOA COCOA)
	find_library(COREFOUNDATION CoreFoundation)
	include_directories(${COCOA} ${COREFOUNDATION} ${PROJECT_SOURCE_DIR}/src)
else()
	include_directories(${PROJECT_SOURCE_DIR}/src)
endif()
add_library(trashcan trashcan.c)
