find_package(Catch2 CONFIG REQUIRED)

set(TEST_NAMES
    test_pixels
    test_image
    test_io
)

foreach(TEST_NAME ${TEST_NAMES})
    add_executable(${TEST_NAME} ${TEST_NAME}.cpp)
    add_test(NAME ${TEST_NAME} COMMAND ${TEST_NAME}
             WORKING_DIRECTORY "${PROJECT_BINARY_DIR}/test")
    target_link_libraries(${TEST_NAME} PRIVATE pnm++ Catch2::Catch2 Catch2::Catch2WithMain)
endforeach(TEST_NAME)
