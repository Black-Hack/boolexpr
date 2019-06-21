cmake_minimum_required(VERSION 3.10)

project(boolexpr)

set(VERSION 2.4)

file(GLOB_RECURSE boolexpr_srcs "src/*.cc")
file(GLOB_RECURSE glucosamine_srcs "third_party/glucosamine/src/core/Solver.cc")

add_library(boolexpr ${boolexpr_srcs} ${glucosamine_srcs})

set_target_properties(boolexpr PROPERTIES
    CXX_STANDARD 17
    CXX_STANDARD_REQUIRED ON
    CXX_EXTENSIONS OFF
)

target_include_directories(boolexpr PUBLIC include)
target_include_directories(boolexpr PUBLIC third_party/glucosamine/src)
