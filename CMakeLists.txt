cmake_minimum_required(VERSION 3.30.4)
project(ghpel VERSION 0.0.0)

# Debugging Settings (uncomment) :
#add_compile_options(-Wall -Wextra -Wpedantic)

# Set C++ 23 Support
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED True)

configure_file(TutorialConfig.h.in TutorialConfig.h)

# Complie to executables
#add_executable(print print.cpp)

add_executable(Tutorial tutorial.cxx)

# add the binary tree to the search path for include files
# so that we will find TutorialConfig.h
target_include_directories(Tutorial PUBLIC
                           "${PROJECT_BINARY_DIR}"
                           )

#add_executable(first tutorial.cxx)

# Linux Builds:
# mkdir build
# cd build
# cmake .. 
# make