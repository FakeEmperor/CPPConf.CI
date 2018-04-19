CMAKE_MINIMUM_REQUIRED(VERSION 2.8.9)
PROJECT (CPPConf_RUSSIA_CONF)

include_directories(./src/include)
file(GLOB SOURCES "./src/main.cpp")

add_executable(hello ./src/main.cpp)