project(obs-amf-tests)

include_directories(SYSTEM ${CMAKE_SOURCE_DIR}/libobs)

set(obs-amf-test_SOURCES
	obs-amf-test.cpp)

add_executable(obs-amf-test
	${obs-amf-test_SOURCES})
target_link_libraries(obs-amf-test
	d3d11
	dxgi
	dxguid)

set_target_properties(obs-amf-test PROPERTIES FOLDER "plugins/obs-ffmpeg")

install_obs_core(obs-amf-test)
