cmake_minimum_required(VERSION 3.4)
project(formatter_ex)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(FORMATTER_LIB_PATH ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib)

add_subdirectory(${FORMATTER_LIB_PATH} ${CMAKE_BINARY_DIR}/formatter_lib)
add_library(formatter_ex STATIC ${CMAKE_CURRENT_SOURCE_DIR}/formatter_ex.cpp)

target_include_directories(formatter_ex PRIVATE
  ${CMAKE_CURREMNT_SOURCE_DIR}
  ${FORMATTER_LIB_PATH}
)

target_link_libraries(formatter_ex formatter)
