# How to use

'''
mkdir ros_ws
cd ros_ws
mkdir src
cd src
git clone https://github.com/adayimaxiga/autonomous-mobile-robot.git
cd ..
catkin_make_isolated
'''
依赖包主要是cartographer的依赖，可以直接 
'''
sudo apt-get install ros-melodic-cartographer
'''

all launch files under  ./tools/launch


# 测试branch and bound scan match 用于amcl闭环检测

在tools/launch目录下

启动gazebo仿真环境，这里有个gui选项，用于选择是否开启gazebo环境，我默认选false因为太卡了  
roslaunch environment.launch  

启动amcl定位算法  
roslaunch amcl.launch  

启动键盘控制  
roslaunch keyboard_control.launch  

启动闭环检测  
roslaunch loop_closure_check.launch  

启动rviz，在tools/rviz  
rviz -d look.rviz  


键盘动一动就看出来了
LD
2019.3.19