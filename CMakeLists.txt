cmake_minimum_required(VERSION 3.0)
project(cjinja)

add_subdirectory(deps/ejson)

add_library(${PROJECT_NAME} cjinja.cpp)
target_include_directories(${PROJECT_NAME}
        PRIVATE $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
        PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
)
target_link_libraries(${PROJECT_NAME} ejson)