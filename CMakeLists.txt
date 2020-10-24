set(IMGUI_SOURCE
        imgui.h
        imstb_rectpack.h
        imstb_textedit.h
        imstb_truetype.h
        imgui_internal.h
        misc/cpp/imgui_stdlib.h
        )

set(IMGUI_HEADER
        imgui.cpp
        imgui_draw.cpp
        imgui_widgets.cpp
        misc/cpp/imgui_stdlib.cpp
        )

add_library(imgui STATIC ${IMGUI_SOURCE} ${IMGUI_HEADER})

target_include_directories(imgui
        PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}
        PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/misc/cpp
        )