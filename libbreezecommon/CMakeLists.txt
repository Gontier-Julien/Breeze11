################# dependencies #################
### Qt/KDE
find_package(Qt5 REQUIRED CONFIG COMPONENTS Widgets)

################# breezestyle target #################
set(breeze11common_LIB_SRCS
    breezeboxshadowrenderer.cpp
)

add_library(breeze11common5 ${breeze11common_LIB_SRCS})

generate_export_header(breeze11common5
    BASE_NAME breezecommon
    EXPORT_FILE_NAME breezecommon_export.h)

target_link_libraries(breeze11common5
    PUBLIC
        Qt::Core
        Qt::Gui)

set_target_properties(breeze11common5 PROPERTIES
    VERSION ${PROJECT_VERSION}
    SOVERSION ${PROJECT_VERSION_MAJOR})

install(TARGETS breeze11common5 ${KDE_INSTALL_TARGETS_DEFAULT_ARGS} LIBRARY NAMELINK_SKIP)
