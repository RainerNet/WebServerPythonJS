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
    src/ui/console_window.cc
    src/ui/flow_graph_window.cc
    src/ui/open_file_modal.cc
    src/ui/about_modal.cc
    )

# Get the current branch we're building
find_package(Git)
if (GIT_FOUND)
  message("Found git ${GIT_EXECUTABLE}")
endif(GIT_FOUND)
message(${CMAKE_CURRENT_SOURCE_DIR})
execute_process(
    COMMAND "\"${GIT_EXECUTABLE}\" rev-parse --abbrev-ref HEAD -- | head -n1"
    RESULT_VARIABLE RESULT
    OUTPUT_VARIABLE MD_BRANCH
    )
if (RESULT EQUAL 0)
  message("Detected branch ${MD_BRANCH}")
else()
  set(MD_BRANCH "UN