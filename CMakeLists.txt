project(antlr-runtime)
set(CMAKE_CXX_STANDARD 20)
file(GLOB_RECURSE ANTLR_SOURCES ./*.cpp ./*.h)
add_library(antlr-runtime ${ANTLR_SOURCES})
set(ANTLR_RUNTIME_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR} PARENT_SCOPE)
target_include_directories(antlr-runtime PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_include_directories(antlr-runtime PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/antlr-runtime)
