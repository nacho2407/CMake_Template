add_executable(test test.cpp)

target_compile_options(test PRIVATE -Wall -Werror)
target_include_directories(test PUBLIC ${CMAKE_SOURCE_DIR}/include)
target_link_libraries(test PRIVATE test_lib)

install(TARGETS test DESTINATION ${CMAKE_SOURCE_DIR}/bin)
