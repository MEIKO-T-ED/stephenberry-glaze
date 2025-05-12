message(">>>> JSON (glaze) <<<<")

add_library(glaze INTERFACE)

target_sources(glaze INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/glaze/glaze.hpp)

target_include_directories(glaze PUBLIC INTERFACE
                     $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
                     $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/glaze>
                     )
