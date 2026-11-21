cmake_minimum_required(VERSION 3.22)

add_compile_options(-fdiagnostics-color=always)

set(RMAKER_PATH ${CMAKE_CURRENT_LIST_DIR}/../components/esp-rainmaker)

set(EXTRA_COMPONENT_DIRS
        ${CMAKE_CURRENT_LIST_DIR}/../ch9_common
        ${CMAKE_CURRENT_LIST_DIR}/../components/esp-idf-lib/components
        ${RMAKER_PATH}/components/esp-insights/components
        ${RMAKER_PATH}/components
        ${RMAKER_PATH}/examples/common)

set(PROJECT_VER "1.0")
include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(sensor)
