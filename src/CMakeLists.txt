# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(dart_libass_library VERSION 0.0.1 LANGUAGES C)

add_library(dart_libass SHARED
  "dart_libass.c"
)

set_target_properties(dart_libass PROPERTIES
  PUBLIC_HEADER dart_libass.h
  OUTPUT_NAME "dart_libass"
)

target_compile_definitions(dart_libass PUBLIC DART_SHARED_LIB)
