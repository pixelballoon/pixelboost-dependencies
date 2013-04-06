cmake_minimum_required (VERSION 2.8.10)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -w")

include_directories("lib")
include_directories("vendor/NSXReturnThrowError")

set (SOURCES
	"lib/DDHidAppleRemote.m"
	"lib/DDHidDevice.m"
	"lib/DDHidElement.m"
	"lib/DDHidEvent.m"
	"lib/DDHidJoystick.m"
	"lib/DDHidKeyboard.m"
	"lib/DDHidKeyboardBarcodeScanner.m"
	"lib/DDHidMouse.m"
	"lib/DDHidQueue.m"
	"lib/DDHidUsage.m"
	"lib/DDHidUsageTables.m"
	"lib/NSDictionary+DDHidExtras.m"
	"vendor/NSXReturnThrowError/NSXReturnThrowError.m"
	)

add_library (ddhidlib ${PIXELBOOST_LIBRARY_TYPE} ${SOURCES})
