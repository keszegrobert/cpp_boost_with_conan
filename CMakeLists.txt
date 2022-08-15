cmake_minimum_required(VERSION 3.16)

project(helloboost VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(Boost_NO_WARN_NEW_VERSIONS ON)

find_package(Boost 1.79.0 COMPONENTS program_options REQUIRED)

add_executable(helloboost
    main.cpp
)

target_link_libraries(helloboost PRIVATE Boost::program_options )
