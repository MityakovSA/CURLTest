cmake_minimum_required(VERSION 3.6)
project(Response_Code)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

find_package(OpenSSL REQUIRED)
find_package(CURL REQUIRED)

add_executable(Response_Code main.cpp)

target_link_libraries(Response_Code ${CURL_LIBRARY} ${OPENSSL_LIBRARIES})