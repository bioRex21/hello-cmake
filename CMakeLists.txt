cmake_minimum_required(VERSION 3.0.0)
project(hello_my_cmake VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(hello_my_cmake src/main.cpp src/includes/MyClass.cpp src/includes/MyClass.h)
include_directories (src/includes)
set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
