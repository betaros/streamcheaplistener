cmake_minimum_required(VERSION 3.22)
project(streamcheaplistener)

set(CMAKE_CXX_STANDARD 20)

find_package(nlohmann_json 3.10.5 REQUIRED)

add_executable(streamcheaplistener main.cpp keylistener/keylistener_win.cpp keylistener/keylistener_win.h keylistener/keylistener_linux.cpp keylistener/keylistener_linux.h keylistener/keylistener_mac.cpp keylistener/keylistener_mac.h)
target_link_libraries(streamcheaplistener PRIVATE nlohmann_json::nlohmann_json)
