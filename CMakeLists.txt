cmake_minimum_required(VERSION 3.23)
project(SteamVR_overlay C)

set(CMAKE_C_STANDARD 99)

link_directories(${PROJECT_SOURCE_DIR})
include_directories(${PROJECT_SOURCE_DIR})

find_package(OpenGL REQUIRED)
find_library(openvr_api.lib openvr_api.lib)
find_library(openvr_api.dll openvr_api.dll)


#find_package(openvr_api.lib REQUIRED)
#target_link_libraries(openvr_api.lib openvr_api.lib)

add_executable(SteamVR_overlay main.c)


include_directories( ${OPENGL_INCLUDE_DIRS} )
target_link_libraries(SteamVR_overlay ${OPENGL_LIBRARIES} )

#set(sources
#        openvr_api.dll
#        steam_api.dll
#        openvr_api.dll
#        openvr_capi.h)
#
#add_library(SteamVR_overly ${sources})
#
#target_link_libraries(C:\\Users\\f-sam\\CLionProjects\\SteamVR_overlay SteamVR_overly)

