project(gmime)

cmake_minimum_required(VERSION 3.5)

file(GLOB_RECURSE H_FILES  CONFIGURE_DEPENDS "gmime/*.h")
file(GLOB_RECURSE C_FILES  CONFIGURE_DEPENDS "gmime/*.c")

add_library(gmime ${H_FILES} ${C_FILES})
target_link_libraries(gmime PUBLIC glib::glib)
