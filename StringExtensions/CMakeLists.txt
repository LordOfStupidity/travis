# CMakeLists.txt for String Extensions

cmake_minimum_required(VERSION 3.8)
set(This StringExtensions)

set(Headers
    include/StringExtensions/StringExtensions.hpp
)

set(Sources
    src/StringExtensions.cpp
)

add_library(${This} STATIC ${Sources} ${Headers})
set_target_properties(${This} PROPERTIES
    FOLDER Libraries
)

target_include_directories(${This} PUBLIC include)

add_subdirectory(test)
