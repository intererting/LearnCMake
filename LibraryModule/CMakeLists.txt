add_library(LibraryModule STATIC module.cpp)

target_include_directories(LibraryModule
        INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}
        )

option(USE_MODULE "Use tutorial provided module implementation" ON)