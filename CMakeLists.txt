cmake_minimum_required(VERSION 3.10)
project(VoxelEngine)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(SDL2 REQUIRED)

include_directories(
    ${SDL2_INCLUDE_DIRS}
    include
)

add_executable(voxel
    src/main.cpp
    src/glad.c
)

target_link_libraries(voxel
    ${SDL2_LIBRARIES}
    GL
)

