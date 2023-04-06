cmake_minimum_required(VERSION 3.16)
project(VkCube)

set(_target "VkCube")
set(_src_dir "${CMAKE_CURRENT_SOURCE_DIR}")
set(_exe_source_list
   ${_src_dir}/cube.c
)

add_executable(${_target} ${_exe_source_list})

target_include_directories(${_target}
   PRIVATE
      /usr/include
)

target_link_libraries(${_target}
   PRIVATE
      m
      vulkan
)


