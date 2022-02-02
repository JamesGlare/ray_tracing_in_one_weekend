cmake_minimum_required(VERSION 3.10.2)
project("ray_tracing")
set(CMAKE_CXX_FLAGS_DEBUG "-g -Wall -Wextra")
set(CMAKE_CXX_FLAGS_RELEASE "-O3")
set(CMAKE_VERBOSE_MAKEFILE ON)

include_directories(
                    "${PROJECT_SOURCE_DIR}/inc"
                    "${PROJECT_SOURCE_DIR}/src"
)
file(GLOB all_SRCS
        "${PROJECT_SOURCE_DIR}/inc/*.h"
        "${PROJECT_SOURCE_DIR}/inc/*.hpp"
        "${PROJECT_SOURCE_DIR}/src/*.cpp"
        "${PROJECT_SOURCE_DIR}/src/*.c"
)
add_executable("${PROJECT_NAME}" ${all_SRCS})