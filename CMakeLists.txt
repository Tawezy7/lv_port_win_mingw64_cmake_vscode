cmake_minimum_required (VERSION 3.22)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_PROJECT_NAME main)

project(${CMAKE_PROJECT_NAME})

#include(${CMAKE_CURRENT_LIST_DIR}/lib/SDL2-2.30.7/cmake/sdl2-config.cmake)

aux_source_directory(./src ALL_SOURCE)

add_executable(${CMAKE_PROJECT_NAME})

target_sources(${CMAKE_PROJECT_NAME} PRIVATE
    ${ALL_SOURCE}
)
target_include_directories(${CMAKE_PROJECT_NAME} PUBLIC
    inc
)

add_subdirectory(lib/cmake-lvgl)

#target_include_directories(${CMAKE_PROJECT_NAME} PRIVATE ${SDL2_INCLUDE_DIRS})
target_link_libraries(${CMAKE_PROJECT_NAME} PRIVATE 
    #${SDL2_LIBRARIES}
    lvgl
    )

