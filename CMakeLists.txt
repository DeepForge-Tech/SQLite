cmake_minimum_required (VERSION 3.21)
 
project(SQLite)
 
set(SOURCE_FILES 
    ./src/shell.c
    ./src/sqlite3.c
)
set(HEADER_FILES 
    ./src/sqlite3.h
    ./src/sqlite3ext.h
)
# And also we specify dependence on static library
add_library(SQLite STATIC ${HEADER_FILES} ${SOURCE_FILES})