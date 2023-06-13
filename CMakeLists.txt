cmake_minimum_required(VERSION 3.0.2)
project(xsens_mvn_ros_msgs)

find_package(catkin REQUIRED COMPONENTS 
    message_generation 
    std_msgs
    geometry_msgs
)

add_message_files(
    DIRECTORY msg
    FILES
    LinkState.msg
    LinkStateArray.msg
)

generate_messages(DEPENDENCIES std_msgs geometry_msgs)

catkin_package(CATKIN_DEPENDS 
    message_runtime 
    std_msgs
    geometry_msgs
)