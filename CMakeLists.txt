cmake_minimum_required (VERSION 2.6)

project(wifi-portal C)

add_definitions(-O -Wall -Werror --std=gnu99)

add_executable(wifi-portal main.c commandline.c conf.c utils.c debug.c http.c)

target_link_libraries(wifi-portal evmongoose ev)

install(TARGETS wifi-portal
	LIBRARY DESTINATION lib
	RUNTIME DESTINATION bin
)
