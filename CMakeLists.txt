cmake_minimum_required(VERSION 2.4)
project(Minisat)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/bin)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/lib)

include_directories(.)

add_executable(minisat
        simp/Main.cc
        simp/SimpSolver.cc
        #core/Main.cc
        core/Solver.cc
        utils/Options.cc
        utils/System.cc
        )
target_link_libraries(minisat z)
