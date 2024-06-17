cmake_minimum_required(VERSION 3.11)

project(QuickJSFFI VERSION 1.0 LANGUAGES C)

find_package(quickjs REQUIRED)

add_library(quickjs-ffi MODULE quickjs-ffi.c)

target_link_libraries(quickjs-ffi
    PRIVATE quickjs
    PRIVATE dl
    PRIVATE ffi
)
