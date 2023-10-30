cmake_minimum_required(VERSION 3.19...3.28)

project(FortranCoarrayExamples
LANGUAGES C Fortran
)

enable_testing()

list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

if(NOT MSVC)
  add_compile_options(-Wall)
endif()

find_package(Coarray REQUIRED)

add_subdirectory(src)

file(GENERATE OUTPUT .gitignore CONTENT "*")
