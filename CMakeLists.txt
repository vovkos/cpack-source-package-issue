project(cpack_source_package_issue)

cmake_minimum_required(VERSION 3.4)

set(VERSION_MAJOR 1)
set(VERSION_MINOR 0)
set(VERSION_PATCH 0)

add_subdirectory(src)

#...............................................................................

set(CPACK_PACKAGE_VERSION_MAJOR ${VERSION_MAJOR})
set(CPACK_PACKAGE_VERSION_MINOR ${VERSION_MINOR})
set(CPACK_PACKAGE_VERSION_PATCH ${VERSION_PATCH})

set(CPACK_SOURCE_GENERATOR TXZ)
set(CPACK_SOURCE_IGNORE_FILES "/[.];/build/")
set(CPACK_SOURCE_PACKAGE_FILE_NAME test-${VERSION_MAJOR}.${VERSION_MINOR}.${VERSION_PATCH}-src)

include(CPack)

#...............................................................................
