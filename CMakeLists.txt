cmake_minimum_required(VERSION 3.22)

project(nghttp2_asio-example LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Threads REQUIRED)
find_package(OpenSSL COMPONENTS Crypto SSL REQUIRED)
find_package(Boost REQUIRED system thread regex)

set(ENABLE_ASIO_LIB ON)
set(ENABLE_APP OFF)
set(ENABLE_HPACK_TOOLS OFF)
set(ENABLE_EXAMPLES OFF)
set(ENABLE_PYTHON_BINDINGS OFF)

add_subdirectory(nghttp2)
add_subdirectory(server)
add_subdirectory(client)

