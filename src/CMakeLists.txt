#find_library(cryptolib NAMES CRYPTO
#        PATHS ${CMAKE_SOURCE_DIR})
#
#if(NOT cryptolib)
#    message( " library not found")
#    else()
#    message( " library found")
#
#endif()
#message( ${cryptolib})

include(buffer/buffer.cmake)
include(algo/algo.cmake)
add_library(data_types_v0_0_0 validator.h configexception.h
        ${Buffer}
        ${CAlgo})
target_link_libraries(data_types_v0_0_0 PUBLIC utilslib CRYPTO)
target_include_directories(data_types_v0_0_0 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})