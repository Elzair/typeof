cmake_minimum_required(VERSION 3.3)

project(boost_typeof)

add_library(boost_typeof INTERFACE)

target_include_directories(boost_typeof BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_typeof DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::typeof ALIAS boost_typeof)
