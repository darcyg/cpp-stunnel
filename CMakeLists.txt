#Specify the version being used
cmake_minimum_required(VERSION 2.8)

#Name your project here
project(cpp-stunnel)

# compiler
SET(CMAKE_CXX_COMPILER "g++")

# cpp flags
SET(CMAKE_CXX_FLAGS "-I/usr/local/include -L/usr/local/lib  -O0 -g -Wall -fmessage-length=0")

# source files
set(CLIENT_SRC "stunnel-client.cpp")

# executable file
add_executable(stunnel-client.exe ${CLIENT_SRC})

# link libraries
target_link_libraries(stunnel-client.exe boost_program_options boost_system) 

