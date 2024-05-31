cmake_minimum_required(VERSION 3.20)

project(planning)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/bin)

# dynamic lib
aux_source_directory(${PROJECT_SOURCE_DIR}/src SRC_LISTS)
add_library(common
SHARED
${SRC_LISTS}
)

target_include_directories(common 
PUBLIC 
${PROJECT_SOURCE_DIR}/include
)

# exe file
add_executable(planning_main planning_main.cpp)

target_include_directories(planning_main
PUBLIC 
${PROJECT_SOURCE_DIR}/include
)

#link
target_link_libraries(planning_main
PUBLIC
common
)
