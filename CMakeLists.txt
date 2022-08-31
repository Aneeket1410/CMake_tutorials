cmake_minimum_required(VERSION 3.22.1)

project(Hello_world LANGUAGES CXX)

add_executable(Hello_World main.cpp)

set(MYVAR "Hey there!")

message("${PROJECT_NAME}")
# message("${PROJECT_NAME_FOO}")

function(print var)
	message("${var} = ${${var}}")
endfunction()

macro(print_list)
	foreach(var ${ARGN})
		message("${var} = ${${var}}")
	endforeach()
	set(MYVAR "Universe")
endmacro()

print(PROJECT_NAME)
print(PROJECT_NAME_FOO)

print_list(PROJECT_NAME PROJECT_NAME_FOO MYVAR)
print(MYVAR)