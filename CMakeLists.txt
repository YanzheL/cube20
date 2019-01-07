cmake_minimum_required(VERSION 3.5)
project(cube20)

set(CMAKE_CXX_STANDARD 17)

add_executable(
        cubepos_test
        cubepos_test.cpp
        cubepos.cpp
)

add_executable(
        kocsymm_test
        kocsymm_test.cpp
        kocsymm.cpp
        cubepos.cpp
)

add_executable(
        phase1prune_test
        phase1prune_test.cpp
        phase1prune.cpp
        phase1prune.h
        kocsymm.cpp
        kocsymm.h
        cubepos.h
        cubepos.cpp
)

add_executable(
        twophase
        twophase.cpp
        phase1prune.cpp
        phase1prune.h
        phase2prune.cpp
        phase2prune.h
        kocsymm.cpp
        kocsymm.h
        cubepos.cpp
        cubepos.h
)

add_executable(
        hcoset
        hcoset.cpp
        phase1prune.cpp
        phase1prune.h
        kocsymm.cpp
        kocsymm.h
        cubepos.cpp
        cubepos.h
        bestsol.h
        corner_order.h
)
target_link_libraries(hcoset pthread)
