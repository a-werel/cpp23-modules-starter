cmake_minimum_required(VERSION 4.4)
set(
    CMAKE_EXPERIMENTAL_CXX_IMPORT_STD
    "f35a9ac6-8463-4d38-8eec-5d6008153e7d"
)
project(chapter0-test LANGUAGES CXX)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
add_executable(MyProgram)
target_sources(MyProgram PRIVATE my_program.cpp)
set_property(
    TARGET MyProgram
    PROPERTY CXX_MODULE_STD ON
)