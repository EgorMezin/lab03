cmake_minimum_required(VERSION 3.4)
project(hello_world)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(FORMATTER_EX_PATH ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib)
set(FORMATTER_PATH ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib)

add_executable(hello_world hello_world.cpp)

target_include_directories(hello_world
    PRIVATE
        /home/egor/EgorMezin/workspace/projects/lab03/lab03/formatter_ex_lib
)

target_link_libraries(hello_world
    ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib/build/libformatter_ex.a
    ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib/build/libformatter.a
)
