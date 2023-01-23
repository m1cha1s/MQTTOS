file(GLOB SRC *.c)

add_library(MQTTOS
    ${SRC}
)

target_include_directories(MQTTOS PRIVATE ${CMAKE_CURRENT_LIST_DIR}/.)