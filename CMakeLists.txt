CMAKE_MINIMUM_REQUIRED(VERSION 2.8.9)
PROJECT (hello CXX)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

include_directories(include)

set(${PROJECT_NAME}_SRC
        src/hello.cpp
        )

add_library(${PROJECT_NAME} ${${PROJECT_NAME}_SRC})

set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD 14)

enable_testing()
add_subdirectory(test)
