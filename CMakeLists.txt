cmake_minimum_required (VERSION 2.8)

project (exactgeodesic)

find_package (Boost REQUIRED)
include_directories (${Boost_INCLUDE_DIRS})

file (GLOB SRC_FILES "src/*.cpp")
file (GLOB HEADER_FILES "include/*.h")
include_directories (include)

add_library (geodesic SHARED ${SRC_FILES} ${SRC_FILES})
