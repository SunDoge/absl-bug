cmake_minimum_required(VERSION 3.15)

project(absl_bug LANGUAGES CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 17)

add_subdirectory(third_party/abseil-cpp)

add_executable(main src/main.cpp)

target_include_directories(main PRIVATE third_party/abseil-cpp)

target_link_libraries(main absl::base absl::flags)