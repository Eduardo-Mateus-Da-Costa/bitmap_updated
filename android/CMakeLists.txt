cmake_minimum_required(VERSION 3.22)

add_library( bitmap

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../ios/Classes/bitmap.cpp )


set(CMAKE_POSITION_INDEPENDENT_CODE ON)
target_link_options(bitmap PRIVATE -Wl,-z,max-page-size=16384)