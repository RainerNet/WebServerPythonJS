cmake_minimum_required(VERSION 3.12)
project(client)

set(CMAKE_CXX_STANDARD 14)

# The main application sources

set(SOURCES
    src/main.cc
    src/machine_decompiler.cc
    src/data/binary.cc
    src/data/log_output.cc
    src/data/hexdump_cache.cc
    src/ui/manager.cc
    src/ui/element.cc
    src/ui/window.cc
    src/ui/modal.cc
    src/ui/ribbon.cc
    src/ui/functions_window.cc
    src/ui/strings_window.cc
    src/ui/disasm_window.cc
    src/ui/hexdump_window.cc
    src/ui/conso