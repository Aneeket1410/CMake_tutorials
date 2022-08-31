cmake_minimum_required(VERSION 3.22.1)

project(Hello_world LANGUAGES CXX)

add_executable(Hello_World main.cpp)

set(MYVAR "Hey there!")

message("${PROJECT_NAME}")

function(print var)
	message("${var} = ${${var}}")
endfunction()

macro(print_list)
	foreach(${ARGN})
		message("${var} = ${${var}}")
	endforeach()
	set(MYVAR "Universe")
endmacro()

