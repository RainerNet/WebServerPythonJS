cmake_minimum_required(VERSION 3.12)
project(client)

set(CMAKE_CXX_STANDARD 14)

# The main application sources

set(SOURCES
    src/main.cc
    src/machine_decompiler.cc
    src/data/b