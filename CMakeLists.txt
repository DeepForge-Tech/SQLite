cmake_minimum_required (VERSION 3.18)
project(SQLite)
find_package (Threads)
set(BUILD_EXAMPLES ON)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/src/include)
set(SOURCE_FILES 
    src/shell.c
    src/sqlite3.c
)
set(HEADER_FILES 
    src/include/sqlite3.h
    src/include/sqlite3ext.h
)
# And also we specify dependence on static library
add_library(SQLite STATIC ${HEADER_FILES} ${SOURCE_FILES})
target_link_libraries(SQLite PRIVATE Threads::Threads)
#if (BUILD_EXAMPLES)
#add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/examples/Connect)
#endif()