cmake_minimum_required(VERSION 3.0.2)
project(my_opencv_tutorial)

find_package(catkin REQUIRED COMPONENTS
  cv_bridge
  image_transport
  roscpp
  sensor_msgs
  std_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES my_pcl_tutorial
#  CATKIN_DEPENDS pcl_conversions pcl_ros roscpp sensor_msgs
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(cv_bridge src/cv_bridge.cpp)

target_link_libraries(cv_bridge
  ${catkin_LIBRARIES}
)
