cmake_minimum_required(VERSION 2.8)

project(TestTask)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(${PROJECT_NAME} "main.cpp")

add_subdirectory(srs)
add_subdirectory(include)

target_include_directories(${PROJECT_NAME} PUBLIC
    include
    srs
)
