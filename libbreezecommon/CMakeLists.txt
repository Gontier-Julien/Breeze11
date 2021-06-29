################# dependencies #################
### Qt/KDE
find_package(Qt5 REQUIRED CONFIG COMPONENTS Widgets)

################# breezestyle target #################
set(breeze10common_LIB_SRCS
    breezeboxshadowrenderer.cpp
)

add_library(breeze10common5 ${breeze10common_LIB_SRCS})

generate_export_header(breeze10common5
    BASE_NAME breezecommon
    EXPORT_FILE_NAME breezecommon_export.h)

target_link_libraries(breeze10common5
    PUBLIC
        Qt::Core
        Qt::Gui)

set_target_properties(breeze10common5 PROPERTIES
    VERSION ${PROJECT_VERSION}
    SOVERSION ${PROJECT_VERSION_MAJOR})

install(TARGETS breeze10common5 ${KDE_INSTALL_TARGETS_DEFAULT_ARGS} LIBRARY NAMELINK_SKIP)
