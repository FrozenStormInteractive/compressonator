cmake_minimum_required(VERSION 3.10)

add_library(Compressonator STATIC "")

file(GLOB_RECURSE CMP_SRCS
     "./*.h"
     "./*.cpp"
     "ASTC/*.h"
     "ASTC/*.cpp"
     "ASTC/ARM/*.h"
     "ASTC/ARM/*.cpp"
     "ATC/*.h"
     "ATC/*.cpp"
     "ATI/*.h"
     "ATI/*.cpp"
     "ATI/*.c"
     "BASIS/*.h"
     "BASIS/*.cpp"
     "BC6H/*.h"
     "BC6H/*.cpp"
     "BC7/*.h"
     "BC7/*.cpp"
     "Block/*.h"
     "Block/*.cpp"
     "Buffer/*.h"
     "Buffer/*.cpp"
     "DXT/*.h"
     "DXT/*.cpp"
     "DXTC/*.h"
     "DXTC/*.cpp"
     "DXTC/*.c"
     "ETC/*.h"
     "ETC/*.cpp"
     "ETC/etcpack/*.h"
     "ETC/etcpack/*.cpp"
     "ETC/etcpack/*.cxx"
     "GT/*.h"
     "GT/*.cpp"
     "Common/*.h"
     "Common/*.cpp"
     "../CMP_Framework/Common/*.h"
     "../CMP_Framework/Common/*.cpp"
     "../CMP_Framework/Common/half/*.h"
     "../CMP_Framework/Common/half/*.cpp"
     "../Applications/_Plugins/Common/ATIFormats.cpp"
     "../Applications/_Plugins/Common/ATIFormats.h"
     )

target_sources(Compressonator
               PRIVATE
               ${CMP_SRCS}
               )
target_include_directories(Compressonator
                           PRIVATE
                           ./
                           ASTC
                           ASTC/ARM/
                           ATC
                           ATI
                           BASIS
                           BC6H
                           BC7
                           Block
                           Buffer
                           DXT
                           DXTC
                           ETC
                           ETC/etcpack/
                           GT
                           Common
                           ../CMP_Framework/Common
                           ../CMP_Framework/Common/half
                           ../Applications/_Plugins/Common)
