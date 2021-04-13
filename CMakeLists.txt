cmake_minimum_required(VERSION 3.0.0)
project(lvgl_demo VERSION 0.1.0)

include(CTest)
enable_testing()

# Includes and libraries
set(SDL2_DIR ${CMAKE_SOURCE_DIR}/lib/SDL2/SDL2-2.0.10)

find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIRS})

# subdirectories
add_subdirectory(lib/lvgl/lv_examples)
add_subdirectory(lib/lvgl/lv_drivers)
add_subdirectory(lib/lvgl/lvgl)

add_executable(lvgl_demo main.c mouse_cursor_icon.c)
target_link_libraries(lvgl_demo lv_examples lv_drivers lvgl ${SDL2_LIBRARIES}) #注意链接顺序，前面依赖后面

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
