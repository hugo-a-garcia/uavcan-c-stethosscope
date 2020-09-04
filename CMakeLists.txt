cmake_minimum_required(VERSION 3.0.0)
project(uavcan-c-node VERSION 0.1.0)

include(CTest)
enable_testing()

include_directories(libcanard socketcan) 
add_executable(uavcan-c-example ./src/main.c libcanard/canard.c socketcan/socketcan.c)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
set(CMAKE_C_STANDARD 11)
include(CPack)
