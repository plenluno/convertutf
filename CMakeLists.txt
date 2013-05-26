# Copyright (c) 2013 Plenluno All rights reserved.

cmake_minimum_required(VERSION 2.8)

project(convertutf)

add_library(convertutf STATIC
    ConvertUTF.cpp
)

if(UNIX AND LIBJ_USE_CXX11)
	set_target_properties(convertutf PROPERTIES
   		COMPILE_FLAGS ${libj-deps-cflags}
   	)
endif(UNIX AND LIBJ_USE_CXX11)
