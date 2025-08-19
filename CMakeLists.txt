cmake_minimum_required(VERSION 3.10)

project(FmtExample)

find_package(fmt CONFIG REQUIRED)

add_executable(FmtExample main.cpp)
target_link_libraries(FmtExample PRIVATE fmt::fmt)

install(DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/$<CONFIG>/ DESTINATION .)