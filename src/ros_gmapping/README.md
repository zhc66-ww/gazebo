 **1.安装与使用方式** 
 **安装gmapping** 

apt install ros-kinetic-gmapping

 **安装map-server，地图导出工具** 

apt install ros-kinetic-map-server

 **功能包准备** 

gitee地址：https://gitee.com/alen2020/ros_gmapping.git

mbot_description：车体描述文件,urdf

mbot_gazebo：gazebo文件，用于提供虚拟地图

mbot_navigation：gmmping启动包

启动方式

```bash
#启动gazebo，创建虚拟地图
$ roslaunch mbot_gazebo mbot_laser_nav_gazebo.launch
#启动gmpping构图
$ roslaunch mbot_navigation gmapping_demo.launch
#启动车体控制程序
$ roslaunch mbot_teleop mbot_teleop.launch

#保存地图
rosrun map_server map_saver -f mymap