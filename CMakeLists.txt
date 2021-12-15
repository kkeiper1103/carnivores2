cmake_minimum_required(VERSION 3.14)
project(carnivores2)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)

add_executable(carnivores2 WIN32
        Hunt2.cpp
        # Audio.cpp
        Audio_DLL.cpp
        Characters.cpp
        Game.cpp
        Interface.cpp
        # Loading.cpp
        mathematics.cpp
        renderd3d.cpp
        RenderSoft.cpp
        Resources.cpp)

target_link_directories(carnivores2 PUBLIC "C:\\Program Files (x86)\\Microsoft DirectX SDK (June 2010)\\Lib\\x64")
target_link_libraries(carnivores2
        ole32.lib oleaut32.lib odbc32.lib odbccp32.lib kernel32.lib user32.lib gdi32.lib winspool.lib comdlg32.lib
        advapi32.lib shell32.lib uuid.lib winmm.lib ddraw.lib dsound.lib wsock32.lib dxguid.lib d3d9.lib d3dx9.lib)