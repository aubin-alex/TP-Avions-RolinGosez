CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

PROJECT ( TP-Avions )

FIND_PACKAGE( OpenSceneGraph REQUIRED osgDB osgViewer osgGA)

set(EXECUTABLE_OUTPUT_PATH bin)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}-std=c++11")

file(
        GLOB_RECURSE
        source_files
        src/*
)

add_executable( TP-Avions ${source_files})

INCLUDE_DIRECTORIES(${OPENSCENEGRAPH_INCLUDE_DIRS} include)
TARGET_LINK_LIBRARIES(TP-Avions ${OPENSCENEGRAPH_LIBRARIES})
