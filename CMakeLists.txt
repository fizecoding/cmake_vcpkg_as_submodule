cmake_minimum_required(VERSION 3.0.0)

set(CMAKE_TOOLCHAIN_FILE "${CMAKE_CURRENT_SOURCE_DIR}/vcpkg/scripts/buildsystems/vcpkg.cmake"
  CACHE STRING "Vcpkg toolchain file")

project(cmake_vcpkg_as_submodule VERSION 0.1.0)

include(CTest)
enable_testing()


find_package(Eigen3 CONFIG REQUIRED)


#executable file 1
set(exe1_name "exe1_name") 
add_executable(exe1_name main.cpp)
target_link_libraries(exe1_name PRIVATE Eigen3::Eigen)


set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
