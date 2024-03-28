cmake_minimum_required(VERSION 3.18)
project(Connect)
add_executable(Connect src/main.cpp)
target_link_libraries(Connect PRIVATE SQLite)