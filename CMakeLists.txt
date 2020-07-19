cmake_minimum_required(VERSION 3.15)
cmake_policy(VERSION 3.15)

set(CMAKE_OSX_DEPLOYMENT_TARGET "10.10" CACHE STRING "Minimum OS X deployment version")

project(liblmdb)

add_library(lmdb STATIC libraries/liblmdb/mdb.c libraries/liblmdb/midl.c)
set_target_properties(lmdb PROPERTIES PUBLIC_HEADER "libraries/liblmdb/lmdb.h")

INSTALL(TARGETS lmdb)
