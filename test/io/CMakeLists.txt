add_executable( test_cfile test_cfile.cpp )
target_link_libraries( test_cfile fc )

add_executable( test_json test_json.cpp )
target_link_libraries( test_json fc )

add_executable( test_tracked_storage test_tracked_storage.cpp )
target_link_libraries( test_tracked_storage fc )

add_test(NAME test_cfile COMMAND libraries/fc/test/io/test_cfile WORKING_DIRECTORY ${CMAKE_BINARY_DIR})
add_test(NAME test_json COMMAND libraries/fc/test/io/test_json WORKING_DIRECTORY ${CMAKE_BINARY_DIR})
add_test(NAME test_tracked_storage COMMAND libraries/fc/test/io/test_tracked_storage WORKING_DIRECTORY ${CMAKE_BINARY_DIR})


