FILE(GLOB_RECURSE RENDERWARE_SOURCES "src/*.cpp")
FILE(GLOB_RECURSE RENDERWARE_HEADERS "include/*.hpp")

source_group("Header Files" FILES ${RENDERWARE_HEADERS})
source_group("Source Files" FILES ${RENDERWARE_SOURCES})


add_library(rwengine
    ${RENDERWARE_SOURCES}
    ${RENDERWARE_HEADERS}
)

target_link_libraries(rwengine sfml-window GLEW)

include_directories(include /usr/include/bullet)