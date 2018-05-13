CMAKE_MINIMUM_REQUIRED(VERSION 3.0.2)
project(sotest)

add_library(static ./test.cpp)
add_library(shared SHARED ./test.cpp)

add_executable(sharedexe ./main.cpp)
add_executable(staticexe ./main.cpp)

target_link_libraries(sharedexe shared)
target_link_libraries(staticexe static)
