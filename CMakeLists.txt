cmake_minimum_required(VERSION 3.10)
project(first_window)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find required packages
find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

# Add GLAD
add_subdirectory(third_party/glad)

# Add executable
add_executable(two_triangles two_triangles.cpp)

# Link libraries
target_link_libraries(two_triangles
    PRIVATE
    OpenGL::GL
    glad
    glfw
    dl
)

# Add executable
add_executable(blinking_triangle blinking_triangle.cpp)

# Link libraries
target_link_libraries(blinking_triangle
    PRIVATE
    OpenGL::GL
    glad
    glfw
    dl
)

# Add executable
add_executable(three_colors_triangle three_colors_triangle.cpp)

# Link libraries
target_link_libraries(three_colors_triangle
    PRIVATE
    OpenGL::GL
    glad
    glfw
    dl
)