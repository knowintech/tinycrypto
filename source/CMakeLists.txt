CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
PROJECT(TinyCrypto-DEBUG C)

SET(PROJ_NAME "TinyCrypto-DEBUG")

#---------------------------------------------------------------------------------------
#
# include dir
#
#---------------------------------------------------------------------------------------
SET(SOURCE_ROOT ${PROJECT_SOURCE_DIR}/src)
SET(TINY_ROOT ${PROJECT_SOURCE_DIR}/../../tiny)

INCLUDE_DIRECTORIES(${SOURCE_ROOT})

INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/TinyBase)
INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/TinyPortable)
INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/TinyContainer)
INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/TinyLog)
INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/TinyStringUtil)
INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/TinyRandom)
INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/TinyBuffer)
INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/StringArray)
INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/Netty)
INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/HttpClient)
INCLUDE_DIRECTORIES(${TINY_ROOT}/source/src/Json)

#---------------------------------------------------------------------------------------
#
# link dir
#
#---------------------------------------------------------------------------------------
LINK_DIRECTORIES(${TINY_ROOT}/target)

#-------------------------------------------------------------------------------------
# output dir
#-------------------------------------------------------------------------------------
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/target)
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/target)
MESSAGE(STATUS "executable output:  ${EXECUTABLE_OUTPUT_PATH}")
MESSAGE(STATUS "library output: ${LIBRARY_OUTPUT_PATH}")

#-------------------------------------------------------------------------------------
#
# Source
#
#-------------------------------------------------------------------------------------
ADD_SUBDIRECTORY(src)
