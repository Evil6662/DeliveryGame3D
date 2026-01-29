cmake_minimum_required(VERSION 3.10)

project(DeliveryGame3D)

set(CMAKE_CXX_STANDARD 17)

# Add the main executable
add_executable(DeliveryGame3D main.cpp)

# Link OpenGL libraries
find_package(OpenGL REQUIRED)
find_package(GLM REQUIRED)
find_package(glfw3 REQUIRED)

# Include directories
include_directories(${OPENGL_INCLUDE_DIRS} ${GLM_INCLUDE_DIRS} ${GLFW_INCLUDE_DIRS})

# Link libraries
target_link_libraries(DeliveryGame3D ${OPENGL_LIBRARIES} glfw Glad glm)