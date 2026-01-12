# Set the minimum version and project name
cmake_minimum_required(VERSION 3.14)
project(VulkanEngine)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find Vulkan
find_package(Vulkan REQUIRED)

set(GLFW_DIR "C:/Users/Yamen/Documents/Visual Studio 2022/Libraries/glfw-3.4.bin.WIN64")
set(GLM_DIR "C:/Users/Yamen/Documents/Visual Studio 2022/Libraries")
set(GLFW_LIBRARY ${GLFW_DIR}/lib-vc2019/glfw3.lib)


include_directories(${GLFW_DIR}/include ${GLM_DIR} )

# Add the source files
add_executable(main main.cpp)

# Link Vulkan to the executable
target_link_libraries(main Vulkan::Vulkan ${GLFW_LIBRARY})
