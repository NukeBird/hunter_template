cmake_minimum_required(VERSION 3.7)

include("cmake/HunterGate.cmake")

HunterGate(
    URL "https://github.com/cpp-pm/hunter/archive/v0.23.275.tar.gz"
    SHA1 "0952a54dc983ecbea09dfe8c53ee65d1e0e91232"
)

project(SUPER_PROJECT)

set(CMAKE_CXX_STANDARD 14)

file(GLOB PROJECT_SOURCE_FILES
    "src/*.h"
    "src/*.hpp"
    "src/*.cpp"
)

add_executable(${PROJECT_NAME} ${PROJECT_SOURCE_FILES})
