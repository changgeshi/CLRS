project(counting_sort)
file(RELATIVE_PATH rel ${CMAKE_BINARY_DIR} ${PROJECT_BINARY_DIR})
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/out/${rel}/bin )
aux_source_directory(./src SRC)

include_directories(./header)
add_executable(counting_sort_test ${SRC} ./test/counting_sort_test.cpp)
target_link_libraries(counting_sort_test gtest gtest_main gmock pthread)
