CMAKE_MINIMUM_REQUIRED(VERSION 2.8.12)

include(ExternalProject)

ExternalProject_Add(breakpad
	SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}
	CONFIGURE_COMMAND ${CMAKE_CURRENT_SOURCE_DIR}/configure --prefix=/usr/local CFLAGS=-std=c99
	BINARY_DIR ${CMAKE_CURRENT_BINARY_DIR}/cmake-build
	BUILD_COMMAND make
	INSTALL_COMMAND sudo make install
	)



