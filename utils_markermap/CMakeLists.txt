include_directories(${PROJECT_SOURCE_DIR}/src ${GNULIBS_INCLUDE_DIR})
link_libraries(${PROJECT_NAME} ${ARUCO_REQUIRED_LIBRARIES} )

add_executable(aruco_create_markermap aruco_create_markermap.cpp)
add_executable(aruco_simple_markermap aruco_simple_markermap.cpp)
add_executable(aruco_test_markermap aruco_test_markermap.cpp pcdwriter.cpp)
add_executable(aruco_markermap_pix2meters aruco_markermap_pix2meters.cpp)


install(TARGETS
  aruco_markermap_pix2meters
  aruco_create_markermap
  aruco_simple_markermap
  aruco_test_markermap
  RUNTIME DESTINATION bin)

