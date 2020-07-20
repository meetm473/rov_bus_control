cmake_minimum_required(VERSION 2.8.3)
project(rov_bus_control)

find_package(catkin REQUIRED COMPONENTS roscpp std_msgs sensor_msgs geometry_msgs nav_msgs)
catkin_package()

if(CATKIN_ENABLE_TESTING)
  find_package(roslaunch REQUIRED)
endif()

include_directories(${catkin_INCLUDE_DIRS})

install(DIRECTORY config meshes models launch src scripts urdf worlds
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

add_executable(rov_control src/rov_control.cpp)
target_link_libraries(rov_control ${catkin_LIBRARIES})
