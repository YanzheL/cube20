cmake_minimum_required(VERSION 3.5)
project(cube20)

set(CMAKE_CXX_STANDARD 14)

add_library(
        cube20 SHARED
        cubepos.h
        cubepos.cpp
        kocsymm.h
        kocsymm.cpp
        phase1prune.cpp
        phase1prune.h
        phase2prune.cpp
        phase2prune.h
)

add_executable(
        cubepos_test
        cubepos_test.cpp
)

add_executable(
        kocsymm_test
        kocsymm_test.cpp
)

add_executable(
        phase1prune_test
        phase1prune_test.cpp
        phase1prune.h
        kocsymm.h
        cubepos.h
)

add_executable(
        phase2prune_test
        phase2prune_test.cpp
        phase2prune.h
        kocsymm.h
        cubepos.h
)

add_executable(
        twophase
        twophase.cpp
        phase1prune.h
        phase2prune.h
        kocsymm.h
        cubepos.h
)

add_executable(
        hcoset
        hcoset.cpp
        phase1prune.h
        kocsymm.h
        cubepos.h
        bestsol.h
        corner_order.h
)

target_link_libraries(cubepos_test cube20)
target_link_libraries(phase1prune_test cube20)
target_link_libraries(phase2prune_test cube20)
target_link_libraries(kocsymm_test cube20)
target_link_libraries(twophase pthread cube20)
target_link_libraries(hcoset pthread cube20)
