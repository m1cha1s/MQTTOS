project(lua)

file(GLOB LUASRC lua/*.c)
list(REMOVE_ITEM LUASRC ${CMAKE_CURRENT_LIST_DIR}/lua/onelua.c)
list(REMOVE_ITEM LUASRC ${CMAKE_CURRENT_LIST_DIR}/lua/lua.c)

add_library(lua
    ${LUASRC}
)

target_include_directories(lua PUBLIC ${CMAKE_CURRENT_LIST_DIR}/lua)
target_link_libraries(lua PRIVATE m)