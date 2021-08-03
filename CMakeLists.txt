cmake_minimum_required(VERSION 3.5)

project(test_c17 LANGUAGES CXX)

find_package(Threads REQUIRED)

add_executable(${PROJECT_NAME}
	main.cpp
	)

set_target_properties(${PROJECT_NAME} PROPERTIES
	CXX_STANDARD 17
	CXX_STANDARD_REQUIRED ON
	CXX_EXTENSIONS OFF
	)

target_link_libraries(${PROJECT_NAME}
	Threads::Threads
	)
