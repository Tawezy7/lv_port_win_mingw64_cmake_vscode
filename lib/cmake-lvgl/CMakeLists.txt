cmake_minimum_required(VERSION 3.22)

project(lvgl)
add_library(lvgl INTERFACE)

# Enable CMake support for ASM and C languages
enable_language(C ASM)

target_compile_definitions(lvgl INTERFACE 
    LV_CONF_INCLUDE_SIMPLE
)

target_include_directories(lvgl INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}/../
)

set(LVGL_ROOT_DIR ${CMAKE_CURRENT_SOURCE_DIR}/../lvgl)

file(GLOB_RECURSE SOURCES ${LVGL_ROOT_DIR}/src/*.c)
file(GLOB_RECURSE EXAMPLE_SOURCES ${LVGL_ROOT_DIR}/examples/*.c)
file(GLOB_RECURSE DEMO_SOURCES ${LVGL_ROOT_DIR}/demos/*.c)

target_sources(lvgl INTERFACE
    ${SOURCES}
    ${EXAMPLE_SOURCES}
    ${DEMO_SOURCES}
)

target_link_directories(lvgl INTERFACE
)

target_link_libraries(lvgl INTERFACE
)
