cmake_minimum_required(VERSION 3.10)
project(gmock-demo)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package(GTest REQUIRED)

enable_testing()

add_executable(email_test test.cpp UserRegistration.cpp)
target_link_libraries(email_test PRIVATE GTest::gmock_main)

include(GoogleTest)
gtest_discover_tests(email_test)