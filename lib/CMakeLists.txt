add_library(test_lib SHARED test_lib.cpp)

target_compile_options(test_lib PRIVATE -Wall -Werror)
target_include_directories(test_lib PUBLIC ${CMAKE_SOURCE_DIR}/include)

install(TARGETS test_lib
    RUNTIME DESTINATION ${CMAKE_SOURCE_DIR}/bin
    LIBRARY DESTINATION ${CMAKE_SOURCE_DIR}/bin
    ARCHIVE DESTINATION ${CMAKE_SOURCE_DIR}/lib
)
