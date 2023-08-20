cmake_minimum_required(VERSION 3.10)

project(AbyssEngine)

# Specify the path to your SDL2 installation
set(SDL2_PATH "C:/Users/aaron/OneDrive/Desktop/SOE/solid-octo-enigma/Engine/libs/SDL2") 


# Set the SDL2 include and library paths
set(SDL2_INCLUDE_DIRS ${SDL2_PATH}/include)
set(SDL2_LIBRARIES 
    ${SDL2_PATH}/lib/x64/SDL2.lib
    ${SDL2_PATH}/lib/x64/SDL2main.lib
)

# Add the SDL2 include directory for your project
include_directories(${SDL2_INCLUDE_DIRS})

# Define the source files for your project
set(SOURCES
    src/main.cpp
)

# Create an executable for your project
add_executable(AbyssEngine ${SOURCES})

# Link SDL2 to your project
target_link_libraries(AbyssEngine ${SDL2_LIBRARIES})

