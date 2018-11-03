cmake_minimum_required(VERSION 3.1)

project(pippo)
add_executable(pippo1 pippo1.c)
add_executable(pippo2 pippo2.c)

install( TARGETS pippo1 DESTINATION bin1 COMPONENT pip1)
install( TARGETS pippo2 DESTINATION bin2 COMPONENT pip2)

set(CPACK_GENERATOR "ZIP")
set(CPACK_PACKAGE_DESCRIPTION_SUMMARY "My funky project")
set(CPACK_PACKAGE_VENDOR "Me, myself, and I")
set(CPACK_PACKAGE_VERSION_MAJOR "1")
set(CPACK_PACKAGE_VERSION_MINOR "3")
set(CPACK_PACKAGE_VERSION_PATCH "2")
set(CPACK_DEBIAN_PACKAGE_MAINTAINER "gigio@giogio")
set(CPACK_ARCHIVE_COMPONENT_INSTALL ON)
set(CPACK_DEB_COMPONENT_INSTALL ON)
include(CPack)

cpack_add_install_type(TypePippo1)
cpack_add_install_type(TypePippo2)

# Component groups
cpack_add_component_group(Pippo1Group)
cpack_add_component_group(Pippo2Group)

# Components
cpack_add_component(pip1
	DISPLAY_NAME "Pippo1 pip Application"
	DESCRIPTION "An extremely useful application that makes use of Pippo1"
	GROUP Pippo1Group
	INSTALL_TYPES TypePippo1
	)

cpack_add_component(pip2
	DISPLAY_NAME "Pippo2 pip Application"
	DESCRIPTION "An extremely useful application that makes use of Pippo2"
	GROUP Pippo2Group
	INSTALL_TYPES TypePippo2
	)
