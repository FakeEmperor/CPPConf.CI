CMAKE_MINIMUM_REQUIRED(VERSION 2.8.9)
PROJECT (CPPConf_RUSSIA_CONF CXX)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

include_directories(include)
target_link_libraries(${PROJECT_NAME} ${CONAN_LIBS})

set(${PROJECT_NAME}_SRC
        src/hello.cpp
)

add_library(${PROJECT_NAME} ${${PROJECT_NAME}_SRC})

set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD 14)
