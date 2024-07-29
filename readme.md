# SQLite
SQLite with CMake Compatibility out of the box, I mainly created this to allow for use in my package manager [cpkg](https://github.com/bonsall2004/cpkg) but also, it's useful.

## Include with CMake
Including in your project:

```cmake
cmake_minimum_required(VERSION 3.10)
project(sqlite-example LANGUAGES C)

add_subdirectory(sqlite) # change this depending on where you store your dependencies

add_executable(sqlite-example main.c)
target_link_libraries(sqlite-example PRIVATE sqlite)
 # the include directories are public so they should be accessible from linking the library

```

By default this is a shared library, to make it static add this flag to your CMake command:
```
-DSQLITE_STATIC
```

## License

SQLite is in the [Public Domain](https://en.wikipedia.org/wiki/Public_domain) 

