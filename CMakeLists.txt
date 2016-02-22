cmake_minimum_required(VERSION 2.8.3)
project(robotis_op_moveit)

find_package(catkin REQUIRED COMPONENTS
moveit_core
cmake_modules
)
catkin_package(
  DEPENDS Eigen
)

include_directories(${Eigen_INCLUDE_DIRS})


install(DIRECTORY launch DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY config DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
