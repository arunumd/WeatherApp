cmake_minimum_required(VERSION 3.15)
project(WeatherApp)

set(CMAKE_CXX_STANDARD 14)

set(CURL_LIBRARY "-lcurl")
find_package(CURL REQUIRED)
add_executable(WeatherApp main.cpp)
include_directories(${CURL_INCLUDE_DIR})
target_link_libraries(WeatherApp ${CURL_LIBRARIES})
