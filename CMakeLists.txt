cmake_minimum_required(VERSION 3.15)

project( BlueSignRecognition )

set (CMAKE_CXX_STANDARD 11)
find_package( OpenCV 3.2 REQUIRED )
add_executable( 
    blueSignRecognition
    MyApplication.cpp
    Utilities.cpp
)
target_link_libraries( blueSignRecognition ${OpenCV_LIBS} )