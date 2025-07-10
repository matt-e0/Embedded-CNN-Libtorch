cmake_minimum_required(VERSION 3.5 FATAL_ERROR)
project(torch_project)

set(CMAKE_CXX_STANDARD 17)

# Replace this path with the actual path to your libtorch
set(Torch_DIR "C:/libtorch/share/cmake/Torch")

find_package(Torch REQUIRED)

add_executable(main main.cpp)
target_link_libraries(main "${TORCH_LIBRARIES}")
set_property(TARGET main PROPERTY CXX_STANDARD 17)
