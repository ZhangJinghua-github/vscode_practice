cmake_minimum_required(VERSION 3.30)

project(Helloworld LANGUAGES CXX C)

add_library(a
    src/a.cpp
)

add_executable(main
    src/main.cpp
    src/a.cpp
)
target_include_directories(main PRIVATE include)
target_link_libraries(main PRIVATE a)