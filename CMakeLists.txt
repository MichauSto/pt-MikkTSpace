
file(GLOB_RECURSE src "./*.c" "./*.h")

project(MikkTSpace VERSION 0.1.0)

add_library(MikkTSpace OBJECT ${src})
set_target_properties(MikkTSpace PROPERTIES LINKER_LANGUAGE CPP)

target_include_directories(MikkTSpace INTERFACE ".")

source_group(TREE "${CMAKE_CURRENT_SOURCE_DIR}" FILES ${src})
