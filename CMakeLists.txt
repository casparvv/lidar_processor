cmake_minimum_required(VERSION 3.0.2)
project(lidar_processor)

find_package(catkin REQUIRED COMPONENTS
  pcl_conversions
  pcl_ros
  roscpp
  sensor_msgs
)

catkin_package(
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_executable(lidar_processor src/lidar_processor.cpp)

target_link_libraries(lidar_processor ${catkin_LIBRARIES})

