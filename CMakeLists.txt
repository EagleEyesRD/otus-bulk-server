cmake_minimum_required(VERSION 3.5)
project(bulk-server)

find_package(Boost REQUIRED)

include_directories(${Boost_INCLUDE_DIR})

set(CMAKE_CXX_STANDARD 14)

add_executable(bulk-server main.cpp)


if(MSVC)
    add_definitions(-D_SCL_SECURE_NO_WARNINGS)
endif()