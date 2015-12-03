cmake_minimum_required(VERSION 3.0)
project(cpp_kata)

find_package(GTest REQUIRED)
include_directories(${gtest_SOURCE_DIRS})

add_definitions(-std=c++11)

add_executable(calculator_test calculatorTest.cpp calculator.h calculator.cpp)
target_link_libraries(calculator_test ${GTEST_LIBRARIES} pthread)

