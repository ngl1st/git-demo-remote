cmake_minimum_required(VERSION 3.23)
project(lanelet2_tutorials)

set(CMAKE_CXX_STANDARD 17)

find_package(lanelet2_core REQUIRED)
find_package (Eigen3 3.3 REQUIRED NO_MODULE)

file(GLOB SOURCE_FILES RELATIVE .  "*.cpp")

message("${SOURCE_FILES}" status)

add_executable(01_dealing_with_lanelet_pritimives 01_dealing_with_lanelet_pritimives.cpp)

target_include_directories(01_dealing_with_lanelet_pritimives PUBLIC ${lanelet2_core_INCLUDE_DIRS})
target_link_libraries(01_dealing_with_lanelet_pritimives ${lanelet2_core_LIBRARIES})
target_link_libraries (01_dealing_with_lanelet_pritimives Eigen3::Eigen)