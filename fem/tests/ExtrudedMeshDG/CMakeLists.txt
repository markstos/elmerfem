INCLUDE(test_macros)
INCLUDE_DIRECTORIES(${CMAKE_BINARY_DIR}/fem/src)

CONFIGURE_FILE( AdvReactDG.sif AdvReactDG.sif COPYONLY)

file(COPY ELMERSOLVER_STARTINFO square  DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/")

ADD_ELMER_TEST(ExtrudedMeshDG LABELS matc)
