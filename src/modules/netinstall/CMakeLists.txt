include_directories( ${PROJECT_BINARY_DIR}/src/libcalamaresui )

calamares_add_plugin( netinstall
    TYPE viewmodule
    EXPORT_MACRO PLUGINDLLEXPORT_PRO
    SOURCES
        NetInstallViewStep.cpp
        NetInstallPage.cpp
        widgets/groupselectionwidget.cpp
    UI
        page_netinst.ui
        widgets/groupselectionwidget.ui
    RESOURCES
        netinstall.qrc
    LINK_PRIVATE_LIBRARIES
        calamaresui
        Qt5::Network
        yaml-cpp
    SHARED_LIB
)
