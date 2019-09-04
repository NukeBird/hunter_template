cmake_minimum_required(VERSION 3.7)

include("cmake/HunterGate.cmake")

HunterGate(
    URL "https://github.com/ruslo/hunter/archive/v0.23.214.tar.gz"
    SHA1 "e14bc153a7f16d6a5eeec845fb0283c8fad8c358"
)

project(SUPER_PROJECT)

set(CMAKE_CXX_STANDARD 14)

file(GLOB PROJECT_SOURCE_FILES
    "src/*.h"
    "src/*.hpp"
    "src/*.cpp"
)

add_executable(${PROJECT_NAME} ${PROJECT_SOURCE_FILES})