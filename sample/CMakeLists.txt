add_executable(unicolor unicolor.cpp)
set_target_properties(unicolor
    PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/sample
)
target_link_libraries(unicolor PRIVATE pnm++)

add_executable(mandelbrot mandelbrot.cpp)
set_target_properties(mandelbrot
    PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/sample
)
target_link_libraries(mandelbrot PRIVATE pnm++)
