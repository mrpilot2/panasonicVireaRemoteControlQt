cmake_minimum_required(VERSION 3.15)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_LIST_DIR}/cmake)

include(StandardProjectSettings)
standard_project_settings()

project(
    vieraRemoteControlQt
    LANGUAGES CXX
    VERSION 0.1.0
)

include(CompilerWarnings)
include(StaticAnalyzers)
include(Sanitizers)

add_subdirectory(dependencies)

add_subdirectory(src)

enable_testing()
add_subdirectory(tests)
