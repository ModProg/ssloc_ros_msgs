cmake_minimum_required(VERSION 3.0.2)
project(ssloc_ros_msgs)

find_package(catkin REQUIRED
  COMPONENTS
  message_generation
  std_msgs
)

add_message_files(DIRECTORY msg FILES
  UnitSsl.msg
  UnitSslArray.msg
  UnitSst.msg
  UnitSstArray.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(CATKIN_DEPENDS message_runtime)
