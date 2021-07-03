# Use another ROS robot with SLAM 


### this project is about implement a SLAM RTAB map and simulate custom robot in kitchen world .

### introduction : 

#### In Localization, a robot is provided to map its environment. The robot has access to its movement and sensor data and uses them to estimate its pose. However, there are many applications where there isn't a known map because the area is unexplored or because the surrounding change often; therefore the map is not up to date. In such case, the robot will have to construct a map, and this leads to robotic mapping.



### you must first install all dependencies that's required : 

#### ROS :
<p><code>sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list' && sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116 && sudo apt-get update && sudo apt-get install ros-kinetic-desktop-full && sudo rosdep init && rosdep update && echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc && source ~/.bashrc
</code></p>


#### kinetic : 

<p><code>sudo apt-get install ros-kinetic-rtabmap ros-kinetic-rtabmap-ros && sudo apt-get remove ros-kinetic-rtabmap ros-kinetic-rtabmap-ros
</code></p>

#### RTAB map :

<p><code>cd ~ && git clone https://github.com/introlab/rtabmap.git rtabmap && cd rtabmap/build && cmake .. && make && sudo make install
</code></p>


### to execute a project :

#### to run gazebo : 

<p><code>$ roslaunch fouliex_bot fouliex_world.launch</code></p>

![task2gazebo](https://user-images.githubusercontent.com/56357074/124365559-8f536100-dc51-11eb-8f63-e0cd1de3a7ff.png)


#### to run a RTAB map ( to show a map ) : 
<p><code>$ roslaunch fouliex_bot mapping.launch</code></p>

![task2RTABmap](https://user-images.githubusercontent.com/56357074/124365561-92e6e800-dc51-11eb-9f88-b9e2c94d878d.png)

#### to run Rviz : 
<p><code>$ roslaunch fouliex_bot rviz.launch</code></p>

![task2Rviz](https://user-images.githubusercontent.com/56357074/124365563-967a6f00-dc51-11eb-8257-cb4da5f0360c.png)


to control a moveing of robot , use this command : 
<p><code>$ roslaunch fouliex_bot teleop.launch</code></p>



https://user-images.githubusercontent.com/56357074/124365827-43092080-dc53-11eb-8af6-ed404cb68bd6.mp4









hint : 

 - i take this project from  https://github.com/georgeerol/MapAWorldWithSlamAndACustomRobot  , and try to run it 
 - any problem that appeared to me i solve it by searching in youtube 
 - there were a 2 world ( kitchen world and cafe world ) but i choose a kitchen world 
