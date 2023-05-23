cmake_minimum_required(VERSION 3.12)
project(ImGui)

# Add ImGui source files
set(IMGUI_SOURCES
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_widgets.cpp
    backends/imgui_impl_glfw.cpp
    backends/imgui_impl_opengl3.cpp
    # Add any other ImGui source files here
)

# Add ImGui header files
set(IMGUI_HEADERS
    imgui.h
    imgui_internal.h
    imconfig.h
    backends/imgui_impl_glfw.h
    backends/imgui_impl_opengl3.h
    imstb_rectpack.h
    imstb_textedit.h
    imstb_truetype.h
    # Add any other ImGui header files here
)

# Create the ImGui library
add_library(imgui ${IMGUI_SOURCES} ${IMGUI_HEADERS})

# Set the include directories for ImGui
target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(imgui PUBLIC

    glfw

)
