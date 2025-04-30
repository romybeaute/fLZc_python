cmake_minimum_required(VERSION 3.15)
project(liblzc C)

set(CMAKE_C_STANDARD 99)

# Output the compiled .dylib into the Python package
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/fLZc_python)

add_library(lzc SHARED
    fLZc_python/core/LZ76c.c
    fLZc_python/core/LZ78c.c
    fLZc_python/core/utils.c
)

target_include_directories(lzc PUBLIC fLZc_python/core)
