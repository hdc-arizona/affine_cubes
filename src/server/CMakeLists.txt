# CMakeLists files in this project can
# refer to the root source directory of the project as ${HELLO_SOURCE_DIR} and
# to the root binary directory of the project as ${HELLO_BINARY_DIR}.
cmake_minimum_required (VERSION 2.8.11)
project (ipca)

SET( CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14 -Wno-inconsistent-missing-override" )

# Recurse into the "Hello" and "Demo" subdirectories. This does not actually
# cause another cmake executable to run. The same process will walk through
# the project's entire directory structure.

add_executable (run_server server.cpp ../affine_cube/boundingvolume.cpp ../affine_cube/bvtree.cpp ../affine_cube/Vector.cpp)
target_link_libraries (run_server LINK_PUBLIC boost_system)
