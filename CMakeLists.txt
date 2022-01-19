cmake_minimum_required(VERSION 3.1)
project(tinkerforge-example C)

find_package(tinkerforge-bindings REQUIRED)

add_executable(example_configuration example_configuration.c)
target_link_libraries(example_configuration tinkerforge::bindings)

add_executable(example_callback example_callback.c)
target_link_libraries(example_callback tinkerforge::bindings)
