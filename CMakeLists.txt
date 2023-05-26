cmake_minimum_required(VERSION 3.0)

project(opcua_ns_server)

add_subdirectory(lib/open62541)

add_executable(${PROJECT_NAME} src/main.c)

option(UA_ENABLE_NODESETLOADER "Enable nodesetLoader public API" ON)

target_link_libraries(${PROJECT_NAME} open62541)
