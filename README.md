ud_mesh
=======

This is the tool for generating pcd or ply files using the asus sensor. It is based on RGBDSLAM.

To install:

1. Make sure you have a laptop with dedicated NVIDIA GPU and installed the latest driver and cuda toolkit. If you can get pcl_kinfu_largescale working, then this step is done.
2. Make sure you installed all openni drivers. If you can get data from openni_launch, then this step is done.
3. Create a directory without writing permission problems. For example,mkdir ~/Desktop/workspace. Then, type in terminal: export ROS_PACKAGE_PATH=~/Desktop/workspace:$ROS_PACKAGE_PATH
4. The previous step adds the directtory to ROS_PACKAGE_PATH. You can double check by typing echo $ROS_PACKAGE_PATH. If there are no problems, do git clone https://github.com/qiaosongwang/ud_mesh.git to download the code into the newly created directory.
5. Make sure you can roscd ud_mesh. Then do a rosdep update, rosdep install ud_mesh and rosmake ud_mesh.
6. Install dependency:sudo apt-get install libglew1.5-dev libdevil-dev libsuitesparse-dev

To use:
1. Do roslaunch openni_launch openni.launch to start the kinect sensor frame grabber, then do rosrun ud_mesh ud_mesh
2. Press space or enter to start/stop scanning.

Contact info:
Qiaosong Wang
University of Delaware
qiaosong@udel.edu
