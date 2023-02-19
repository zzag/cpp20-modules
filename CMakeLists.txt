cmake_minimum_required(VERSION 3.25)
project(test CXX)

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_EXPERIMENTAL_CXX_MODULE_DYNDEP 1)
set(CMAKE_EXPERIMENTAL_CXX_MODULE_CMAKE_API "2182bf5c-ef0d-489a-91da-49dbc3090d2a")

if (CMAKE_CXX_COMPILER_ID STREQUAL "Clang")
  include(clang_modules.cmake)
elseif (CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
  include(gcc_modules.cmake)
endif()

add_subdirectory(src)
