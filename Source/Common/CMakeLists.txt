set(BASE_APP_INCLUDE_DIRS 
	${CMAKE_CURRENT_SOURCE_DIR} 
	${CMAKE_CURRENT_SOURCE_DIR}/../../External
CACHE INTERNAL "" FORCE)

include_directories(${BASE_APP_INCLUDE_DIRS})

add_library(base_app STATIC
	${CMAKE_CURRENT_SOURCE_DIR}/Application.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/RayTracingApplication.cpp
)

target_link_libraries(base_app vulkan xcb)
