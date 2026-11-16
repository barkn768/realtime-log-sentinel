cmake_minimum_required(VERSION 3.14)
project(RealtimeLogSentinel VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Threads REQUIRED)
include_directories(include)

add_executable(log_sentinel src/main.cpp)
target_link_libraries(log_sentinel PRIVATE Threads::Threads)