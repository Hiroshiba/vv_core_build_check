cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(check)

# find_package(Torch REQUIRED)
# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${TORCH_CXX_FLAGS}")

add_executable(check check.cpp)
# target_link_libraries(check "${TORCH_LIBRARIES}")
set_property(TARGET check PROPERTY CXX_STANDARD 14)

# if (MSVC)
#   file(GLOB TORCH_DLLS "${TORCH_INSTALL_PREFIX}/lib/*.dll")
#   add_custom_command(TARGET check
#                      POST_BUILD
#                      COMMAND ${CMAKE_COMMAND} -E copy_if_different
#                      ${TORCH_DLLS}
#                      $<TARGET_FILE_DIR:check>)
# endif (MSVC)
