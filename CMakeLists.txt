cmake_minimum_required(VERSION 3.10)
project(sqlite LANGUAGES C)

if(NOT DEFINED SQLITE_STATIC)
  set(SQLITE_BUILD_TYPE SHARED)
else()
  set(SQLITE_BUILD_TYPE STATIC)
endif()

add_library(sqlite ${SQLITE_BUILD_TYPE} src/shell.c src/sqlite3.c)

target_include_directories(sqlite PUBLIC includes)
