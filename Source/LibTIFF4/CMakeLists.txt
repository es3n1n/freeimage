# This file is automatically generated from cmake.toml - DO NOT EDIT
# See https://github.com/build-cpp/cmkr for more information

# Create a configure-time dependency on cmake.toml to improve IDE support
if(CMKR_ROOT_PROJECT)
	configure_file(cmake.toml cmake.toml COPYONLY)
endif()

# Target: libtiff4
set(libtiff4_SOURCES
	tif_aux.c
	tif_close.c
	tif_codec.c
	tif_color.c
	tif_compress.c
	tif_dir.c
	tif_dirinfo.c
	tif_dirread.c
	tif_dirwrite.c
	tif_dumpmode.c
	tif_error.c
	tif_extension.c
	tif_fax3.c
	tif_fax3sm.c
	tif_flush.c
	tif_getimage.c
	tif_jpeg.c
	tif_luv.c
	tif_lzma.c
	tif_lzw.c
	tif_next.c
	tif_ojpeg.c
	tif_open.c
	tif_packbits.c
	tif_pixarlog.c
	tif_predict.c
	tif_print.c
	tif_read.c
	tif_strip.c
	tif_swab.c
	tif_thunder.c
	tif_tile.c
	tif_version.c
	tif_warning.c
	tif_write.c
	tif_zip.c
	cmake.toml
)

add_library(libtiff4)

target_sources(libtiff4 PRIVATE ${libtiff4_SOURCES})
source_group(TREE ${CMAKE_CURRENT_SOURCE_DIR} FILES ${libtiff4_SOURCES})

target_compile_definitions(libtiff4 PUBLIC
	_LIB
)

if((CMAKE_CXX_COMPILER_ID MATCHES "Clang" AND NOT CMAKE_CXX_COMPILER_FRONTEND_VARIANT MATCHES "^MSVC$") OR (CMAKE_C_COMPILER_ID MATCHES "Clang" AND NOT CMAKE_C_COMPILER_FRONTEND_VARIANT MATCHES "^MSVC$")) # clang
	target_compile_options(libtiff4 PUBLIC
		-Wno-everything
	)
endif()

if(CMAKE_CXX_COMPILER_ID STREQUAL "GNU" OR CMAKE_C_COMPILER_ID STREQUAL "GNU") # gcc
	target_compile_options(libtiff4 PUBLIC
		-Wno-everything
	)
endif()

if(MSVC) # msvc
	target_compile_options(libtiff4 PUBLIC
		"/W0"
	)
endif()

target_include_directories(libtiff4 PUBLIC
	.
)

target_link_libraries(libtiff4 PUBLIC
	zlib
	libjpeg
)

