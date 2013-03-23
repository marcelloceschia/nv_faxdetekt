cmake_minimum_required (VERSION 2.6)
project(app_nv_faxdetect)

SET(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/CMakeModules")
find_package(asterisk REQUIRED)

add_library(app_nv_faxdetect SHARED app_nv_backgrounddetect.c app_nv_faxdetect.c)
set_target_properties(app_nv_faxdetect PROPERTIES PREFIX "")

install (TARGETS app_nv_faxdetect DESTINATION ${ASTERISK_LIBRARY_DIR})
