cmake_minimum_required(VERSION 3.25)
project(testIMGUI)

set(CMAKE_CXX_STANDARD 17)
find_package(glfw3 3.3 REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(
        testDearImgui
        main.cpp
        imgui/imgui.cpp imgui/imgui_demo.cpp imgui/imgui_draw.cpp imgui/imgui_tables.cpp imgui/imgui_widgets.cpp
        imgui/imgui_impl_glfw.cpp imgui/imgui_impl_opengl3.cpp
        )

target_link_libraries(testDearImgui glfw)
target_link_libraries(testDearImgui OpenGL::GL)
