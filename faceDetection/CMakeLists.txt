find_package(OpenCV REQUIRED)

include_directories(${OpenCV_INCLUDE_DIR} )
include_directories(${SmartVision_SOURCE_DIR}/common)
link_directories(${SmartVision_BINARY_DIR}/common)
add_library(faceDetection faceDetectionModule.h)

#use libraries of opencv and common
target_link_libraries(faceDetection ${OpenCV_LIBS} common)
set_target_properties(faceDetection PROPERTIES LINKER_LANGUAGE CXX) 
