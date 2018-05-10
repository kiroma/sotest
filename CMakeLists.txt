CMAKE_MINIMUM_REQUIRED(VERSION 3.0.2)
project(sotest)
add_library(mylib SHARED ./test.cpp)
add_executable(myexe ./main.cpp)
target_link_libraries(myexe mylib)

