project(sqlite LANGUAGES C)

add_library(sqlite SHARED src/shell.c src/sqlite3.c)
target_include_directories(sqlite PUBLIC includes)