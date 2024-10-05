cmake_minimum_required(VERSION 3.0)
project(ejson)

FILE(GLOB SOURCE_FILES src/*.cpp include/*.h include/*.hpp)
include_directories(include)
add_library(${PROJECT_NAME} ${SOURCE_FILES})
target_include_directories(${PROJECT_NAME}
        PRIVATE $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
        PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
)