cmake_minimum_required(VERSION 4.4)
set(
    CMAKE_EXPERIMENTAL_CXX_IMPORT_STD
    "f35a9ac6-8463-4d38-8eec-5d6008153e7d"
)
project(cpp23_modules_starter LANGUAGES CXX)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
add_executable(MyProgram)
target_sources(MyProgram 
    PRIVATE 
        my_program.cpp
    
    PRIVATE
        FILE_SET CXX_MODULES
        FILES
            helloworld.cppm
)
set_property(
    TARGET MyProgram
    PROPERTY CXX_MODULE_STD ON
)