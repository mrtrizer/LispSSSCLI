cmake_minimum_required(VERSION 2.8)

project(LispSSSCLI)

set(CMAKE_BUILD_TYPE Debug)

add_definitions("-std=c++1y")
include_directories(
    "./src/"
    "../../src/"
)
add_subdirectory(engine engine)

file(GLOB SOURCES src/*.cpp)

set(EXECUTABLE_NAME LispSSSCLI)

add_executable(${EXECUTABLE_NAME} ${SOURCES})

target_link_libraries(${EXECUTABLE_NAME} LispSSS)

install(TARGETS ${EXECUTABLE_NAME} DESTINATION lispssscli)
install(CODE "execute_process(COMMAND ln -sf ${CMAKE_INSTALL_PREFIX}/lispssscli/${EXECUTABLE_NAME} /usr/local/bin/lispsss)")
