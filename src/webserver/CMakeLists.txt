cmake_minimum_required(VERSION 2.8.3)
project(webserver)

## System dependencies are found with CMake's conventions
find_package(catkin REQUIRED COMPONENTS
    rospy
)

catkin_python_setup()

###################################
## catkin specific configuration ##
###################################
catkin_package(
    CATKIN_DEPENDS rospy
)

###########
## Build ##
###########

include_directories(
    ${catkin_INCLUDE_DIRS}
)

#############
## Install ##
#############

catkin_install_python(PROGRAMS bin/webserver 
    DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
