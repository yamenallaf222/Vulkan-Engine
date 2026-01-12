# Set the minimum version and project name
cmake_minimum_required(VERSION 3.14)
project(VulkanEngine)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find Vulkan
find_package(Vulkan REQUIRED)
add_executable(main main.cpp)

# Link Vulkan to the executable
target_include_directories(main PRIVATE ${CMAKE_SOURCE_DIR}/glfw-3.4.bin.WIN64/include ${CMAKE_SOURCE_DIR})
target_link_libraries(main Vulkan::Vulkan ${CMAKE_SOURCE_DIR}/glfw-3.4.bin.WIN64/lib-vc2019/glfw3.lib)


