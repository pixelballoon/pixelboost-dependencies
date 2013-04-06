cmake_minimum_required (VERSION 2.8.10)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -w")

include_directories("include")

set (SOURCES
	"include/enet/callbacks.h"
	"include/enet/enet.h"
	"include/enet/list.h"
	"include/enet/protocol.h"
	"include/enet/time.h"
	"include/enet/types.h"
	"include/enet/unix.h"
	"include/enet/utility.h"
	"include/enet/win32.h"
	"callbacks.c"
	"compress.c"
	"host.c"
	"list.c"
	"packet.c"
	"peer.c"
	"protocol.c"
	"unix.c"
	"win32.c"
	)

add_library (enet ${PIXELBOOST_LIBRARY_TYPE} ${SOURCES})
