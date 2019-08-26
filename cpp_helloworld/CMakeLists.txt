cmake_minimum_required(VERSION 1.9)
project (hello_world_cmake)
add_executable(hello_world_cmake hello_world_cmake.cpp)
install(TARGETS hello_world_cmake RUNTIME DESTINATION bin)
