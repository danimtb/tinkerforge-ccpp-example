cmake_minimum_required(VERSION 3.1)
project(tinkerforge-example C)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_BINARY_DIR})
list(APPEND CMAKE_PREFIX_PATH ${CMAKE_BINARY_DIR})

find_package(tinkerforge-bindings REQUIRED)


add_executable(example_configuration example_configuration.c)
target_link_libraries(example_configuration tinkerforge::bindings)

add_executable(example_callback example_callback.c)
target_link_libraries(example_callback tinkerforge::bindings)
