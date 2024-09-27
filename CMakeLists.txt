cmake_minimum_required(VERSION 3.10)
project(project-gl)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

include_directories(${PROJECT_SOURCE_DIR}/include)

add_executable(${PROJECT_NAME} main.cpp src/glad.c)

target_link_libraries(${PROJECT_NAME} OpenGL::GL glfw dl)
