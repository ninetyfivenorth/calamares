file( GLOB SUBDIRECTORIES RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "*" )
foreach( SUBDIRECTORY ${SUBDIRECTORIES} )
    set( _sd "${CMAKE_CURRENT_SOURCE_DIR}/${SUBDIRECTORY}" )
    if( IS_DIRECTORY "${_sd}" AND EXISTS "${_sd}/branding.desc" )
        calamares_add_branding_subdirectory( ${SUBDIRECTORY} )
    endif()
endforeach()
