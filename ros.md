# ROS

## Installition



## Navigating the Ros Filesystem

### Using rospack

+ find option : return the path to package

### USing roscd

change a directory directly to a package

### roscd log

take you to the folder where ROS stores log files

### USing rosls

ls directly in a package by name rather than by absolute path

## Creating a ROS package

### make up a catkin package

+ package structure:

```markdown
mypackage/
	CMakeLists.txt
	package.xml
	include/
	src/
```

+ package in a catkin workspace

```markdown
workspace_folder/
	src/
		CMakLists.txt
		package_1/
			CMakeLists.txt
			package.xml
			include/
			src/
		package_n/
			CMakeLists.txt
			package.xml
			include/
			src/
```

+ create a catkin package

  + First: change to the source space directory of th catkin workspace

  + Second: use catkin_create_pkg to create a new package which depends on std_msgs, roscpp, rospy

    ```shell
    catkin_create_pkg beginner_tutorials std_msgs rospy roscpp
    example:
    catkin_create_pkg <package_name> [depend1] [depend2] [depend3]
    ```

+ building a catkin workspace and sourcing the setup file

  + build the packages in the catkin workspace

    ```shell
    cd ~/catkin_ws
    catkin_make
    ```

  + add the workspace to your ROS environment 

    ```shell
    . ~/catkin_ws/devel/setup.bash
    ```

+ customizing own package

  + description tag

    update the description tag:

    ```markdown
    <description>The beginner_tutorials package</description>
    ```

  + maintainer tags: it lets other know who to contact about the package

    ```markdown
    <maintainer email="you@yourdomain.tld">Your Name</maintainer>
    ```

  + license tags

    ```markdown
    <license>BSD</license>
    ```

  + dependencies tags

    The dependencies are spilt into `build_depend`,`buildtool_depend`,`exec_depend`,`test_depend`

  + final paxkage.xml

## Building a ROS Package

### Building Packages

As longas all of the system dependencies of your package are installed, we can now build your own package.Use the following command:

```shell
# source /opt/ros/<your ros distro>/setup.bash
```

+ Using cattkin_make

  catkin_make combines the calls to cmake and make

  + in a CMake workflow, build command:

    ```shell
    $ mkdir build
    $ cd build
    $ cmake ..
    $ make # make install (optionally)
    ```

  + in a catkin workspace,build command:

    ```shell
    $ catkin_make
    ```

+ Building your package

  You should already create a catkin workspace and a new catkin package.

  Then go to the catkin workspace, build the package using catkin_make

  ```shell
  cd ~/catkin_ws
  catkin_make
  ```

  After catkin_make command,there will be three folders in your catkin workspace:

  + build :  is the default location of the build space and is where cmake and make are called to configure and build your packages
  + devel : is the default location of the devel space, which is where your executables and libraries go before you install your package
  + src :

## What is ROS Nodes

### Prerequisites : install a lightweight simulator 

```shell
$ sudo apt-get install ros-<distro>-ros-tutorials  # <sidtro> is your ROS distribution
```

### Graph Concepts

+ Nodes : is an executable that uses ROS to communicate with other nodes
+ Messages : ROS data type used when subsribing or publishing a topic
+ Topics : Nodes can publish messages to a topic as well as subscribe to a topic to receive messages
+ Master : Name service for ROS
+ rosout : ROS equivalent of stdout/stderr
+ roscore : Master + rosout + parameter server

### roscore

roscore is the first thing that should run when using ROS

### Using rosnode

+ **rosode list command** :rosnode displays information about the ROS nodes that are currently running, the rosnode list command lists these active nodes 

+ **rosnode info command** : return information about a special node 

### Using rosrun

rosrun allows you to use the package name to directly run a node within a package

Usage : 

```shell
$ rosrun [package_name] [node_name]
```

We can reassign Names from th command-line, The node list will add a node called  your_name

```shell
$ rosrun [package_name] [node_name] __name:=<your name>
```



## What is ROS topics

### Setup

+ **roscore**

  

+ **turtlesim**

  

+ **turtle keyboard teleoperation**

  

### ROS Topic



