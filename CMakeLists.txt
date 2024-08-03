cmake_minimum_required(VERSION 3.11)

project(Test_Project)

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)
set(CMAKE_INSTALL_RPATH $ORIGIN)

add_subdirectory(lib)
add_subdirectory(src)
add_subdirectory(test)

add_dependencies(main test_lib)
add_dependencies(test test_lib)
