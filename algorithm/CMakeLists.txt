add_library(gnuradio-algorithm INTERFACE)
target_include_directories(gnuradio-algorithm INTERFACE $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include/> $<INSTALL_INTERFACE:include/>)
target_link_libraries(gnuradio-algorithm INTERFACE gnuradio-options gnuradio-meta vir fftw fmt magic_enum)

add_subdirectory(src)

if (ENABLE_TESTING)
    add_subdirectory(test)
endif ()
