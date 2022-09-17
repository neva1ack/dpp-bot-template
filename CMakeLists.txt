cmake_minimum_required(VERSION 3.24)
# reminder: change cmake_cpp_project_template
project(
  cmake_cpp_project_template
  VERSION 0.1.0
  LANGUAGES CXX)
# C++ 17 ISO standard
set(CMAKE_CXX_STANDARD 17)
# Require standard
set(CMAKE_CXX_STANDARD_REQUIRED ON)
# set release build
set(CMAKE_BUILD_TYPE Release)
# create build dir
file(MAKE_DIRECTORY build)
# generate compile_commands.json
set(CMAKE_EXPORT_COMPILE_COMMANDS 1)
# create executable from src/
include_directories(${PROJECT_SOURCE_DIR}/include)
file(GLOB PROJECT_GLOBBED_SOURCES ${PROJECT_SOURCE_DIR}/src/*.cpp)
add_executable(${PROJECT_NAME} ${PROJECT_GLOBBED_SOURCES})
