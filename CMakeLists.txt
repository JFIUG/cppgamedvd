cmake_minimum_required(VERSION 3.10)
project(YourProjectName)

# Set C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Find SFML package
find_package(SFML 2.5 COMPONENTS Graphics Audio REQUIRED)

# Add your source files
set(SOURCES
    source/main.cpp
    # Add more source files here if needed
)

# Add an executable target
add_executable(${PROJECT_NAME} ${SOURCES})

# Include SFML headers
target_include_directories(${PROJECT_NAME} PRIVATE ${SFML_INCLUDE_DIR})

# Link SFML libraries
target_link_libraries(${PROJECT_NAME} PRIVATE sfml-graphics sfml-audio)
