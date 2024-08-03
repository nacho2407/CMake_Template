add_executable(main main.cpp)

target_compile_options(main PRIVATE -Wall -Werror)
target_include_directories(main PUBLIC ${CMAKE_SOURCE_DIR}/include)
target_link_libraries(main PRIVATE test_lib)

install(TARGETS main DESTINATION ${CMAKE_SOURCE_DIR}/bin)
