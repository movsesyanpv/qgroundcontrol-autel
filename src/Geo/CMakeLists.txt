find_package(Qt6 REQUIRED COMPONENTS Core Positioning)

qt_add_library(Geo STATIC
	Constants.hpp
	Math.cpp
	Math.hpp
	MGRS.cpp
	MGRS.hpp
	PolarStereographic.cpp
	PolarStereographic.hpp
	QGCGeo.cc
	QGCGeo.h
	TransverseMercator.cpp
	TransverseMercator.hpp
	Utility.cpp
	Utility.h
	Utility.hpp
	UTMUPS.cpp
	UTMUPS.hpp
)

target_link_libraries(Geo
	PRIVATE
		Qt6::Core
	PUBLIC
		Qt6::Positioning
)

target_include_directories(Geo
	PUBLIC
		${CMAKE_CURRENT_SOURCE_DIR}
)
