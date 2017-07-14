cmake_minimum_required(VERSION 2.6)

project(ezraknet)

file(GLOB_RECURSE RAKNET_SOURCES "src/*.cpp")

if(MSVC)
	add_definitions(-D_CRT_SECURE_NO_WARNINGS)
endif()

add_library(raknet
	"${RAKNET_SOURCES}"
)

target_link_libraries(raknet ws2_32)

target_include_directories(raknet
	PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include"
)

install(TARGETS raknet RUNTIME DESTINATION "${CMAKE_SOURCE_DIR}/bin"
			LIBRARY DESTINATION "${CMAKE_SOURCE_DIR}/lib"
			ARCHIVE DESTINATION "${CMAKE_SOURCE_DIR}/lib")
