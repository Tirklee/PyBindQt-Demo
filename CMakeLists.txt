cmake_minimum_required(VERSION 3.5)
project(PythonQtIntegration)

# Set C++ standard to C++17
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)  # Optional: Disable compiler-specific extensions

# Find Qt6 packages
find_package(Qt6 REQUIRED COMPONENTS Widgets)



# Add pybind11
execute_process(COMMAND git clone --depth 1 https://github.com/pybind/pybind11.git)
add_subdirectory(pybind11)

# Add executable
add_executable(PythonQtIntegration main.cpp)

# Link against Qt and pybind11
target_link_libraries(PythonQtIntegration PRIVATE Qt6::Widgets pybind11::module)
