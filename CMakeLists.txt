project(msgpackc)
cmake_minimum_required(VERSION 3.20)

add_library(msgpackc)
target_compile_options(msgpackc PRIVATE -Wall -Wextra)
set_target_properties(msgpackc PROPERTIES C_STANDARD 11)

target_include_directories(msgpackc PUBLIC include)
add_subdirectory(src)

file(CONFIGURE OUTPUT .gitignore
  NEWLINE_STYLE UNIX
  CONTENT "*")
