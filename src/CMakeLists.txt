project(lrzsz C)
set( C_STANDARD 11 )
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/libs)
add_subdirectory(libs)

set(lrz_SOURCES
    lrz.c
    timing.c
    zperr.c
    zreadline.c
    crctab.c
    rbsb.c
    zm.c
    protname.c
    tcp.c
    lsyslog.c
    canit.c
)
set(lsz_SOURCES
    lsz.c
    timing.c
    zperr.c
    zreadline.c
    crctab.c
    rbsb.c
    zm.c
    protname.c
    tcp.c
    lsyslog.c
    canit.c
)
add_executable(lrz ${lrz_SOURCES})
add_executable(lsz ${lsz_SOURCES})
target_link_libraries(lrz intl)
target_link_libraries(lsz intl)