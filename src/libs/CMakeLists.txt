
project(lrzsz)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SRCS)
add_library(intl STATIC ${SRCS})
