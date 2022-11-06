cmake_minimum_required(VERSION 3.5.0)
project(Lie_test)

set(CMAKE_CXX_STANDARD 11)

find_package(pinocchio)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
add_subdirectory(eigen)

add_executable(load_model load_model.cpp)
target_link_libraries(load_model
    pinocchio
    eigen
)

add_executable(display_robot display_robot.cpp)
target_link_libraries(display_robot
    pinocchio
    eigen
)

