# CMakeLists.txt
cmake_minimum_required(VERSION 3.0)
project(test)

# sqlite not used
find_package(SQLite3 REQUIRED)

find_package(Boost REQUIRED)

include_directories(${Boost_INCLUDE_DIR})

add_executable(main main.cpp)

target_link_libraries(main LINK_PUBLIC ${Boost_LIBRARIES})