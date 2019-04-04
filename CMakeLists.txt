cmake_minimum_required(VERSION 2.8)
project( faceDetection )

set(CMAKE_C_FLAGS -pthread)
set(CMAKE_EXE_LINKER_FLAGS -pthread)

set(OpenCV_DIR "/home/yichuan/Apps/opencv-3.2.0/release/")

#include_directories(${OpenCV_INCLUDE_DIRS})

find_package( OpenCV REQUIRED)
add_executable(webcam_face_pose_ex webcam_face_pose_ex.cpp)
target_link_libraries(webcam_face_pose_ex dlib::dlib ${OpenCV_LIBS} )
