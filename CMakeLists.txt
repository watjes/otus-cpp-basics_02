cmake_minimum_required(VERSION 3.8)

project(hello_world CXX)

add_executable(hello_world hello_world.cpp move_me_out.h move_me_out.cpp)

target_compile_features(hello_world PUBLIC cxx_std_17)

if(MSVC)
    target_compile_options(hello_world PUBLIC /W4 /WX)
else()
    target_compile_options(hello_world PUBLIC -Wall -Wextra -Werror -pedantic)
endif()
