cmake_minimum_required(VERSION 3.12)
project(buttonrpc_cpp14_example)
add_executable(main_client main_client.cpp)
add_executable(main_server main_server.cpp)

target_include_directories(main_client PRIVATE ${PROJECT_SOURCE_DIR}/..)
target_include_directories(main_server PRIVATE ${PROJECT_SOURCE_DIR}/..)

target_link_libraries(main_client zmq)
target_link_libraries(main_server zmq)
