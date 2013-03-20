cmake_minimum_required (VERSION 2.8.10)

include_directories("include")

add_definitions(-DFT2_BUILD_LIBRARY)

set (SOURCES
	"src/base/ftsystem.c"
	"src/base/ftinit.c"
	"src/base/ftdebug.c"
	"src/base/ftbase.c"
	"src/base/ftbbox.c"
	"src/base/ftbitmap.c"
	"src/base/ftglyph.c"
	"src/cff/cff.c"
	"src/sfnt/sfnt.c"
	"src/truetype/truetype.c"
	"src/raster/raster.c"
	"src/smooth/smooth.c"
	"src/autofit/autofit.c"
	"src/pshinter/pshinter.c"
	"src/psnames/psnames.c"
	)

add_library (freetype2 STATIC ${SOURCES})