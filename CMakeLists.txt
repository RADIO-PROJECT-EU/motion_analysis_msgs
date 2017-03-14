cmake_minimum_required(VERSION 2.8.3)
project(motion_analysis_msgs)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  sensor_msgs
  message_generation
)

add_message_files(
  FILES
  shapes_msg.msg
  Point2D.msg
  BoundingBox.msg
  AnswerWithHeader.msg
)

generate_messages(
	DEPENDENCIES
	std_msgs
  sensor_msgs
)

catkin_package(CATKIN_DEPENDS std_msgs)

