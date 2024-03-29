cmake_minimum_required(VERSION 3.5)
project(DS_Alg)

# Set C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Include directories
include_directories(
    ${CMAKE_SOURCE_DIR}/include
    ${CMAKE_SOURCE_DIR}/lib
)

# Find all source files
file(GLOB_RECURSE SOURCES "src/*.cpp" "lib/**/*.cpp")

# Add executable
add_executable(main ${SOURCES})


# Function to recursively find source files
function(add_sources dir)
    file(GLOB children RELATIVE ${CMAKE_SOURCE_DIR}/${dir} ${CMAKE_SOURCE_DIR}/${dir}/*)
    foreach(child ${children})
        if(IS_DIRECTORY ${CMAKE_SOURCE_DIR}/${dir}/${child})
            add_sources(${dir}/${child})
        else()
            if(${child} MATCHES ".*\\.cpp$")
                list(APPEND SOURCES ${dir}/${child})
            elseif(${child} MATCHES ".*\\.h$")
                target_include_directories(main PRIVATE ${CMAKE_SOURCE_DIR}/${dir})
            endif()
        endif()
    endforeach()
endfunction()

# Find all source files
add_sources(lib)

# Set output directory
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/build)

# Set include directories for the project
target_include_directories(main
  PRIVATE
    ${CMAKE_SOURCE_DIR}/include
    ${CMAKE_SOURCE_DIR}/lib  # Include /lib for header files at that level
)

