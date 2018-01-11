cmake_minimum_required(VERSION 2.8)
project( mono-vo )
find_package( OpenCV 3.0 REQUIRED )

include_directories( ${OpenCV_INCLUDE_DIRS} )

file(GLOB viso
    "src/*.h"
    "src/*.cpp"
)
add_executable( vo src/visodo.cpp )
target_link_libraries( vo ${OpenCV_LIBS} )


add_executable( my_vo src/my_vo.cpp )
target_link_libraries( my_vo ${OpenCV_LIBS} )
