cmake_minimum_required(VERSION 3.20)

project(planning)

set(CMAKE_CXX_STANDARD 17)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

aux_source_directory(. SRC_LISTS)

add_executable(palnning_main ${SRC_LISTS})
