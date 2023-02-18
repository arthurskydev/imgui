cmake_minimum_required(VERSION 3.23)

set(CMAKE_CXX_EXTENSIONS 17)
set(CMAKE_CXX_COMPILER_VERSION 17)

project(imgui)

set(SOURCES
        imconfig.h
        imgui.h
        imgui.cpp
        imgui_draw.cpp
        imgui_internal.h
        imgui_widgets.cpp
        imstb_rectpack.h
        imstb_textedit.h
        imstb_truetype.h
        imgui_demo.cpp)


add_library(${PROJECT_NAME} STATIC ${SOURCES})
target_include_directories(${PROJECT_NAME} PUBLIC ${PROJECT_SOURCE_DIR})