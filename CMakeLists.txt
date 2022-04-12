cmake_minimum_required(VERSION 3.12)

project(QtNetworkServiceTest)

set(CMAKE_AUTOMOC ON)
SET(CMAKE_INCLUDE_CURRENT_DIR ON)

find_package(Qt5 COMPONENTS
            Core
            Network
            REQUIRED)

include_directories(${CMAKE_SOURCE_DIR}/src)

add_executable(${PROJECT_NAME} 
    src/HttpClient.h

    sample/main.cpp
)

target_link_libraries(${PROJECT_NAME}
    Qt5::Core
    Qt5::Network
)