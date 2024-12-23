cmake_minimum_required(VERSION 3.10)
project(auto_stream_plugin1)

# OBS Studio'ni sozlash uchun kerakli kutubxonalarni yo'naltirish
set(OBS_DIR "C:/Users/dyhac/obs-studio")  # OBS Studio papkasiga yo'lni to'g'ri sozlang

include_directories(${OBS_DIR}/libobs)
include_directories(${OBS_DIR}/UI)

add_library(auto_stream_plugin1 MODULE main.cpp)

# OBS kutubxonasiga ulanish
target_link_libraries(auto_stream_plugin1 obs)
