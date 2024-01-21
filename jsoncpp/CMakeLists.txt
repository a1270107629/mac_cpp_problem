cmake_minimum_required(VERSION 3.0.0)
project(jscpp VERSION 0.1.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 11)
set(jsoncpp_DIR /opt/homebrew/Cellar/jsoncpp/1.9.5)
# find_package(jsoncpp REQUIRED)
# find_package(jsoncpp REQUIRED
# 			 PATHS /opt/homebrew/Cellar/jsoncpp/1.9.5
# 			 NO_DEFAULT_PATH)
include_directories(${jsoncpp_DIR}/include/json)
link_directories(${jsoncpp_DIR}/lib)

add_executable(jscpp test.cpp)
target_link_libraries(jscpp jsoncpp)
