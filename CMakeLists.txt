cmake_minimum_required(VERSION 3.17)
project(VTKlab)

# Найдём VTK
find_package(VTK REQUIRED)
# ... и подключим её со всеми её компонентами её нативными средствами
include(${VTK_USE_FILE})
set(CMAKE_CXX_STANDARD 14)
add_executable(VTKlab main.cpp)
target_link_libraries(VTKlab ${VTK_LIBRARIES})
target_link_libraries(VTKlab -lgmsh)