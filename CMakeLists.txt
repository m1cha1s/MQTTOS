cmake_minimum_required(VERSION 3.16)

project(MQTTOS)

add_subdirectory(src)
add_subdirectory(inc)
add_subdirectory(lib)

target_link_libraries(MQTTOS PUBLIC lua)