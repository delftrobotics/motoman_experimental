cmake_minimum_required(VERSION 2.8.3)

project(motoman_mh5l_support)

find_package(catkin REQUIRED)

catkin_package()

find_package(roslaunch)
roslaunch_add_file_check(test/launch_test.xml)

install(
	DIRECTORY config launch meshes urdf
	DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
