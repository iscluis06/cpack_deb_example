CMAKE_MINIMUM_REQUIRED(VERSION 3.28)
PROJECT(cmake_pack
    VERSION 1.0.0
)

SET(CMAKE_CXX_STANDARD 11)

ADD_EXECUTABLE(cmake_pack main.cpp)

INSTALL(TARGETS cmake_pack
    RUNTIME DESTINATION ~/bin/${PROJECT_NAME}
)

SET(DESTDIR /tmp/bin/${PROJECT_NAME})
SET(CPACK_SET_DESTDIR ON)

SET(CPACK_PACKAGE_NAME, ${PROJECT_NAME})

SET(CPACK_GENERATOR "DEB;TGZ")

SET(CPACK_PACKAGE_CONTACT "Luis Anaya")

INCLUDE(CPack)