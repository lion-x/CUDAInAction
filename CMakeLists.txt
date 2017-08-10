cmake_minimum_required(VERSION 3.7)
project(CUDAInAction)

set(CMAKE_CXX_STANDARD 11)

FIND_PACKAGE(CUDA)
message(STATUS "CUDA found: ${CUDA_FOUND}")

INCLUDE_DIRECTORIES(inc)

CUDA_ADD_EXECUTABLE(vectorAdd
        vectorAdd.cu)

CUDA_ADD_EXECUTABLE(deviceQuery
        deviceQuery.cpp)
