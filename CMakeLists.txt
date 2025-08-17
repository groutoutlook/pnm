cmake_minimum_required(VERSION 4.0)
enable_testing()
project(pnm++)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(pnm++ INTERFACE)
target_include_directories(pnm++ INTERFACE ${PROJECT_SOURCE_DIR} )

option(PNM_BUILD_SAMPLES "Builds the sample applications" ON)
option(PNM_BUILD_TEST "Builds the tests" ON)

if (PNM_BUILD_SAMPLES)
    add_subdirectory(sample)
endif ()

if (PNM_BUILD_TEST)
    add_subdirectory(test)
endif ()
