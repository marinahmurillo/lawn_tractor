# ros_lawn_tractor
Software for self driving lawn tractor.

![alt text](https://github.com/ros-agriculture/ros_lawn_tractor/blob/master/lawn_tractor.png "ROS Lawn Tractor")

https://www.youtube.com/watch?v=-RF8hOKg6WU

# Install
<pre>
git clone https://github.com/ros-agriculture/ros_lawn_tractor.git 
git clone https://github.com/bsb808/geonav_transform.git

prompt$ rosdep update
prompt$ rosdep install -y --from-paths . --ignore-src --rosdistro ${ROS_DISTRO}
prompt$ cd catkin_ws
prompt/catkin_ws$ catkin build
prompt/catkin_ws$ source devel/setup.bash
prompt/catkin_ws$ roslaunch lawn_tractor_sim lawn_tractor_sim.launch
</pre>

# Docker
Install Docker <br />
If you use Ubuntu Trusty, Wily, or Xenial, install the linux-image-extra kernel package:

<pre>
prompt$ sudo apt-get update -y && sudo apt-get install -y linux-image-extra-$(uname -r)
</pre>

Install Docker:
<pre>
prompt$ sudo apt-get install docker-engine -y
</pre>
Start Docker:
<pre>
prompt$ sudo service docker start
</pre>
Verify Docker:
<pre>
prompt$ sudo docker run hello-world
</pre>

Download Start File
<pre>
prompt$ wget https://github.com/ros-agriculture/ros_lawn_tractor/blob/master/docker/start.sh
prompt$ chmod +x start.sh
prompt$ ./start.sh
</pre>
..... wait for image to download ......
<pre>
docker/prompt$ roslaunch lawn_tractor_sim lawn_tractor_sim.launch
</pre>
