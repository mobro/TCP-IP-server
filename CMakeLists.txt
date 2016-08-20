# Make - Cross Platform Makefile Generator
# Copyright 2000-2012 Kitware, Inc., Insight Software Consortium
#
# Distributed under the OSI-approved BSD License (the "License");
# see accompanying file Copyright.txt for details.
#
# This software is distributed WITHOUT ANY WARRANTY; without even the
# implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
# See the License for more information.
#=============================================================================
cmake_minimum_required(VERSION 2.8.4 FATAL_ERROR)
project(server)

set (CMAKE_EXPORT_COMPILE_COMMANDS 1)
set (CMAKE_CXX_FLAGS_DEBUG "{CMAKE_CXX_FLAGS_DEBUG} -Wall")
set(CMAKE_BUILD_TYPE Debug)

#Generate ctags file
#add_custom_target(ctags
#	COMMAND ctags -o . -R --exclude=.git .)

#set (C_PROJECT_VERSION_MAJOR 0)
#set (C_PROJECT_VERSION_MINOR 1)
#
## configure a  header file to pass some of the CMake settings to the source code
#configure_file(
#	"${PROJECT_SOURCE_DIR}/src/fos/config.h.in"
#	"${PROJECT_BINARY_DIR}/src/fos/config.h")
#
#include_directories("${PROJECT_BINARY_DIR}")

include_directories(src)
add_executable(server src/server.c)
