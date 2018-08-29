cmake_minimum_required(VERSION 3.0)
project(qub3d-libdeps)

option(LIBC "..." ON)

add_subdirectory(SDL2)
set_target_properties (SDL2 PROPERTIES FOLDER "qub3d-libdeps/SDL2")
set_target_properties (SDL2main PROPERTIES FOLDER "qub3d-libdeps/SDL2")
set_target_properties (SDL2-static PROPERTIES FOLDER "qub3d-libdeps/SDL2")
set_target_properties (uninstall PROPERTIES FOLDER "qub3d-libdeps/SDL2")

add_subdirectory(glew/build/cmake)
set_target_properties (glew PROPERTIES FOLDER "qub3d-libdeps/glew")
set_target_properties (glew_s PROPERTIES FOLDER "qub3d-libdeps/glew")

SET(YAML_CPP_BUILD_TESTS OFF CACHE BOOL "Don't build yaml-cpp tests")
add_subdirectory(yaml-cpp)
set_target_properties (format PROPERTIES FOLDER "qub3d-libdeps/yaml-cpp")
set_target_properties (yaml-cpp PROPERTIES FOLDER "qub3d-libdeps/yaml-cpp")
set_target_properties (parse PROPERTIES FOLDER "qub3d-libdeps/yaml-cpp")
set_target_properties (read PROPERTIES FOLDER "qub3d-libdeps/yaml-cpp")
set_target_properties (sandbox PROPERTIES FOLDER "qub3d-libdeps/yaml-cpp")
