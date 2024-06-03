cmake_minimum_required(VERSION 3.22)

add_library(adiosy_platform
    Private/AdLog.cpp
    Private/AdWindow.cpp
    Private/Window/AdGLFWwindow.cpp
)

target_include_directories(adiosy_platform PUBLIC External)

# glfw
option(GLFW_BUILD_DOCS OFF)
option(GLFW_BUILD_TESTS OFF)
option(GLFW_BUILD_EXAMPLES OFF)
option(GLFW_BUILD_TESTS OFF)
option(GLFW_INSTALL OFF)
add_subdirectory(External/glfw)
target_link_libraries(adiosy_platform PRIVATE glfw)

