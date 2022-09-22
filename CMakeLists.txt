cmake_minimum_required(VERSION 3.23)
project(lazy_foo)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_EXE_LINKER_FLAGS "-static")

set(SDL2_DIR ${CMAKE_SOURCE_DIR}/lib/SDL2/cmake)

find_package(SDL2 REQUIRED)
include_directories(lazy_foo ${SDL2_INCLUDE_DIR} )

add_executable(lazy_foo main.cpp)
target_link_libraries(lazy_foo ${SDL2_LIBRARIES})