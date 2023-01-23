cmake_minimum_required(VERSION 3.16)


execute_process(
	COMMAND git submodule update --init
	WORKING_DIRECTORY ${CMAKE_CURRENT_LIST_DIR}
)

project(MQTTOS)

add_subdirectory(src)
add_subdirectory(inc)
add_subdirectory(lib)

target_link_libraries(MQTTOS PUBLIC lua)
