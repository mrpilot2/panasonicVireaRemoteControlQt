add_subdirectory(core)
add_subdirectory(gui)

add_executable(vieraRemoteControlQt)

target_sources(vieraRemoteControlQt
    PRIVATE main.cpp
)

target_link_libraries(vieraRemoteControlQt
    PRIVATE
    Aide::AideApplication
    vieraRemoteGui
    vieraRemoteCore
)
