# anh_robot_description
## robot_links_and_joints.urdf
* For this file, I created the base and the lasers with all the size stated in the lab manual.  
* I also created joints to connect base with all of its children and the origin coordinates and rotation are put into these joints.

## robot_links_and_joints.xacro
* The base link and the joints between base and the lasers are the same as the *robot_links_and_joints.urdf* file.  
* The laser links are created using xacro:laser.
Parents of the lasers, it's origin xyz and rpy and the meshes of laser are also configured in the xacro:laser line.  
* All the wheels are created using xacro:macro code blocks.
I added the <axis /> code blocks into the joints of the wheels so that they can be turned like regular wheels.  

## urdf_from_xacro.urdf
 * This file is created when run
    > rosrun xacro xacro --inorder robot_links_and_joints.xacro > urdf_from_xacro.urdf  
 * All the links and joints necessary for the robot are created based on *robot_links_and_joints.xacro* and
 I built the robot by running the command:
    > rosparam set /robot_description -t urdf_from_xacro.urdf.   
 * instead of running:  
    > rosrun xacro xacro --inorder robot_links_and_joints.xacro | rosparam set /robot_descripiton -
 ## Additional comments
 * Plese disregard the launch folder. My launch file are in src/launch folder.  
 * My [video](https://drive.google.com/file/d/1Cvl9rozws8iZfRCuNR5xTVt-H5eCevPY/view?usp=sharing) 
 of rotating the wheels before configure the axis
 * My [video](https://drive.google.com/file/d/1d1ugP1xWMuflIAFJJYSaQ5TJJABhhS-n/view?usp=sharing) 
 of rotating the wheels after having configured the axis
 
