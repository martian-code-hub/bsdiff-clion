cmake_minimum_required(VERSION 3.23)
file(GLOB bzip bzip/*.c)
project(bsdiff C)

set(CMAKE_C_STANDARD 99)

add_library(bsdiff SHARED main.c bsdiff.c bspatch.c ${bzip} err.c)
