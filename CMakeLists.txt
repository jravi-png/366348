cmake_minimum_required(VERSION 3.1)

project(my_application)

add_subdirectory(module1)
add_subdirectory(module2)

add_executable(application main.cpp)

target_include_directories(application PUBLIC ${module2_SOURCE_DIR})
target_link_libraries(application module2)  