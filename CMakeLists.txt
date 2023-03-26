cmake_minimum_required (VERSION 3.20.3)
# project(cpp-examples)
# find_package( OpenCV REQUIRED )
# MESSAGE( "${OpenCV_INCLUDE_DIRS}" )
# MESSAGE( "${OpenCV_LIBS}" )

# project(displayimage)
# add_executable(displayimage cv-display/displayimage.cpp)
# target_link_libraries( displayimage ${OpenCV_LIBS} )

project(semi-global-matching)
find_package( OpenCV REQUIRED )

FILE(GLOB_RECURSE INCLUDE_FILES SemiGlobalMatching/*.h)
FILE(GLOB_RECURSE SOURCE_FILES SemiGlobalMatching/*.cpp)

add_executable(semi-global-matching main.cpp)
target_link_libraries( semi-global-matching ${OpenCV_LIBS} ${INCLUDE_FILES} ${SOURCE_FILES})

