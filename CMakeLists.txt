cmake_minimum_required(VERSION 3.15)

project( BlueSignRecognition )

set (CMAKE_CXX_STANDARD 17)
find_package( OpenCV 3.2 REQUIRED )
find_package( Boost COMPONENTS filesystem REQUIRED )
INCLUDE_DIRECTORIES( ${Boost_INCLUDE_DIR} )
add_executable( 
    blueSignRecognition
    MyApplication.cpp
    Utilities.cpp
)
target_link_libraries( blueSignRecognition ${OpenCV_LIBS} ${Boost_LIBRARIES} )