cmake_minimum_required (VERSION 2.6)
project(app_nv_faxdetect)

SET(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/CMakeModules")



find_package(asterisk REQUIRED)
# find_library(mp4v2)
# find_library(LIBMP4V2_LIBRARY NAMES mp4v2 DOC "mp4v2 Library")

add_library(app_nv_faxdetect SHARED app_nv_backgrounddetect.c app_nv_faxdetect.c)
set_target_properties(app_nv_faxdetect PROPERTIES PREFIX "")

# target_link_libraries (app_mp4 mp4v2) 


install (TARGETS app_nv_faxdetect DESTINATION ${ASTERISK_LIBRARY_DIR})
