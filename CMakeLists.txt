cmake_minimum_required(VERSION 2.8.9)
project(tangoidl)
include(GNUInstallDirs)

#need to define the version of the library
set(MAJOR_VERSION "6")

#convenient versions
set(LIBRARY_VERSION "${MAJOR_VERSION}.${MINOR_VERSION}.${PATCH_VERSION}")

install(FILES tango.idl DESTINATION "${CMAKE_INSTALL_FULL_INCLUDEDIR}")

configure_file(tangoidl.pc.cmake tangoidl.pc @ONLY)

install(FILES "${CMAKE_CURRENT_BINARY_DIR}/tangoidl.pc"
DESTINATION "${CMAKE_INSTALL_FULL_LIBDIR}/pkgconfig")

