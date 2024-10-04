cmake_minimum_required(VERSION 3.0.2)
project(hw2)

# Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  tf
  gazebo_msgs
)

# Catkin-specific configuration
catkin_package()

# Install Python scripts
catkin_install_python(PROGRAMS scripts/your_script.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

# Ensure that we can find Python modules
include_directories(${catkin_INCLUDE_DIRS})
