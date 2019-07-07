cmake_minimum_required(VERSION 3.14)
project(hello)
set(CMAKE_BUILD_TYPE release)

include_directories(include)
#set(SOURCES src/app.cpp  src/helloworld.cpp)
#aux_source_directory(src SOURCES)

file(GLOB SOURCES "src/*.cpp")

#add_library(hello STATIC ${SOURCES})

#find_package(Opengl REQUIRED)
#include_directories(${OPENGL_INCLUDE_DIRS})
#link_directories(/usr/local/lib)


set(PROJECT_LINK_LIBS hello.dll)
link_directories(build)

#install_targets(TARGET hello DESTINATION _install)
add_executable(hello ${SOURCES})
target_link_libraries(hello ${PROJECT_LINK_LIBS})