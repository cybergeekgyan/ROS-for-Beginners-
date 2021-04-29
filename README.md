# ROS-for-Beginners-
  - *Follow this step by step for full process in detail.*

## What you'll learn
- Understand ROS Ecosystem (topics, nodes, messages, services, actionlib)
- Develop simple applications to control robot motion
- Understand how a position and orientation are represented in ROS
- Recognize how to develop a C++/Python ROS project
- Develop simple computer vision programs with ROS and OpenCV

** Three major topics 👎
- **ROS Basics and Foundation**:  which deals with the general ROS concepts that everyone has to know, like ROS topics, Services, Messages, Nodes, ...

- **Motion in ROS**:
    -  We apply the concepts learned in Step 1 to make a robot move. 
    -  We will develop a different trajectory in the context of a nice example simulating a cleaning robot. 
    -  In particular, we illustrate how to represent the pose (position and orientation) of a robot in ROS, and 
    -  how to send a motion control message to make the robot move. 
    -  We clearly demonstrate how to implement a linear motion, a rotational motion, and spiral motion and 
    -  how all of these be integrated to simulate a cleaning application. 
    -  This part will you the background you need to understand robot kinematics and how motion is represented in ROS.

- **Perception in ROS**: 
    - how a robot sees the environment using a camera, 
    - how the images are collected in ROS, and 
    - how they are processed in OpenCV. 

- **Arduino**:
    - we will also learn how to use Arduino boards and sensors with ROS using the ROSSERIAL Arduino interface. 
    - This will allow you to integrate any Arduino sensor and board into your robot and robotics applications.

![whatisrobot](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/whatisrobot.png)
![impact](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/impact.png)
![hotareas](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/hotareas.png)

**SELF DRIVING CARS**
![selfdrivingcars](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/selfdrivingcars.png)

**DRONES**
![drones](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/drones.png)

**SERVICE ROBOTS**
![servicerobots](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/servicerobots.png)

**INDUSTRIAL ROBOTS**
![industrialrobots](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/industrialrobots.png)


![rpc](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/rpc.png)

![rpc2](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/rpc2.png)

![sense](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/sense.png)

![think](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/think.png)

![act](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/act.png)


## WHAT IS ROS?
![whatisros](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/whatisros.png)

![rosecosystem](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/rosecosystem.png)

![rosdistributions](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/rosdistributions.png)


**WHAT IS ROS?**<br>

▸ ROS is an open-source software framework for robot software development<br> 
▸ Provides an operating system-like functionality<br> 
▸ Provides OS services<br> 
▸ Hardware abstraction <br>
▸ Low-level device control<br>
▸ Implementation of commonly-used functionality<br> 
▸ Message-passing between processes<br>
▸ Package management<br>

**WHY ROS?**<br>

▸ Code reuse in Robotics R&D<br> 
▸ Ready-to-use development environment<br> 
▸ Comprehensive tools and client API libraries<br> 
▸ Scalable (distributed network of processes loosely coupled)<br> 
▸ Large community<br> 
▸ Continuous support<br>

## ROS Installation and Environment Setup 

**which distribution to Install?**
  - visit http://wiki.ros.org/ROS/Tutorials
  - consider a version which supports LTS(Long Time Support) avoid version which dont have long time support
  - Lunar doesn't have LTS while Kinetic, Indigo and Melodic have long time support. so choose wisely according to your need
  - It is suggested to install Kinetic However It is old as compared to Melodic as it contains lots of packages.
  - If you want to go for Melodic, go for it as it is newly released and will have LTS

**ROS Installation**
 - It is highly recommended to install ROS on Ubuntu as it is most stable on UBuntu. It can also be installed on other operating system as well
 - Every version of ROS it works on specific version of Ubuntu.
 - ROS (Melodic) is only supported on Ubuntu 18.04 (Bionic) release.

**Where to Install ROS?**
  - you can have installation of ROS on either 
    * on a physical machine 
        * the problem here is, because of any kind of reason your system crashes, stopped working and  gets damaged. 
        * This requires reinstallation of the whole system which might be a tedious task to do so and also very time consuming. 
        * So instead of installing on a physical machine, *We recommend you to install on a Virtual Machine.*
    * or on a Virtual Machine
        * we recommend using virtual machine for working on ROS.

### Virtual Machine Installation

===> **Installation of Virtual Machine(VM) on different operating system**
    
   * Virtual Machine(VM) for windows
      
      * Download required version of Ubuntu from the official website 
      * Install 7z software to extract the files downloaded
      * Download & Install VMware/VirtualBox from it official website and run it.   
    
   
   * VM for Mac
   
     * Install VM Fusion on mac.


### Ubuntu Installation

===> **Installation of Ubuntu on different operating system**

   * Ubuntu on windows using VMware Workstation Player
      
      * Download the Ubuntu iso (desktop not server) and the free VMware Player.
      * Install VMware Player and run it.
      * Select “Create a New Virtual Machine”
      * Select “Installer disc image file” and browse to the Ubuntu iso you downloaded.
      * You should see that it will use Easy Install – this takes care of most of the hard work for you. Click next
      * Enter your full name, username and password and hit next
      * Select the maximum disk size and type. Unless you’re planning on some really CPU intensive work inside the VM, 
        select the “Split virtual disk into multiple files” option. Hit next when you’re happy with the settings.
      * This brings you to the confirmation page. Click “Customize Hardware”
      * In the hardware options section select the amount of memory you want the VM to use. In this instance I’ve gone for 4GB out of the 16GB installed in my laptop. 
        Leave everything else as it is and click Close.
      * This brings you back to the confirmation page. Click Finish this time
      * You will probably be prompted to download VMware Tools for Linux. Click “Download and Install” to continue
      * Wait for it to install
      * Ubuntu will then start to install, so keep waiting (or do what I did and go to bed!)
      * When all is done you’ll be presented with the Ubuntu login screen. So enter your password and you’re on your way.
      * Click the clock in the top right to set your time and date settings
      * Once you’ve set that up, you’re up and running with Ubuntu in VMware Player on your Windows machine. Congratulations and enjoy
 
   * Ubuntu on Mac using VM Fusion


### Which Integrated Development Environment(ID) to use with ROS
   - There are many alternatives for this purpose such as **Anaconda, Eclipse, Sublime, CLion, Visual Studio Code, Codeblocks, Netbeans, VIM, Qtcreator, Pycharm(community edition), KDevelop, RDS (ROS Development Studio), RoboWare Studio**
 
   * First possible option is to use **Eclipse**
       * when you open Eclipse, you need to open it in the catkin_ws(workspace), select ok when prompted.
       * however Eclipse is little bit slow and also heavy.

   * Second, you can use **SUBLIME TEXT EDITOR**
       * It is a lightweight editor 
       * you don't get an integrated terminal here

   * Third, you can use **Visual Studio Code**(*Recommended*)
       * It supports c++, python and other different programming languages
       * we get an Integrated terminal here , so you can run your code here in the terminal itself
       * It is very lightweight as compared to Eclipse and also simple to use.

## ROS FILE SYSTEM - Hands On

**CONFIGURE WORKSPACE**<br>
▸ source /opt/ros/<ros-distro>/setup.bash<br>
▸ activate the ROS default workspace<br> 
▸ Add the command into .bashrc file<br>
▸ .bashrc is a file executed automatically every time a new terminal is open<br> 
▸ roscd<br>
▸ take you to the default workspace<br> 

▸ cd<br>
▸ takes you to HOME directory<br> 
▸ .bashrc is in the HOME directory<br> 
▸ you can create shortcuts and aliases in .bashrc<br> 
▸ alias gb=“gedit /home/gyan/.bashrc”<br>
*replace gyan by your username*<br>

**Create a ROS workspace**
     
   ▸ create your own catkin workspace (catkin_ws) in your HOME directory<br> 
   ▸ your catkin workspace will be used to create and store your own ROS packages (project)<br> 
   ▸ catkin is the name of the build tool used to compile and execute programs in ROS<br>
  
  *Let's create and build a catkin workspace:*
      
      $ mkdir -p ~/catkin_ws/src
      $ cd ~/catkin_ws/
      $ catkin_make

  ==> The *catkin_make* command is a convenience tool for working with catkin workspaces. 
  Running it the first time in your workspace, it will create a *CMakeLists.txt link* in your *'src'* folder.

 - Additionally, if you look in your current directory you should now have a *'build'* and *'devel'* folder. 
 - Inside the *'devel'* folder you can see that there are now several *setup.*sh* files. 
 - Sourcing any of these files will overlay this workspace on top of your environment. 
 - To understand more about this see the general catkin documentation: catkin. Before continuing source your new setup.*sh file:

       $ source devel/setup.bash
       
 - To make sure your workspace is properly overlayed by the setup script, make sure **ROS_PACKAGE_PATH** environment variable includes the directory you're in.

       $ echo $ROS_PACKAGE_PATH
       /home/youruser/catkin_ws/src:/opt/ros/<ros-distro>/share

### ROS PACKAGE


**CREATE A ROS PACKAGE**<br>
▸ Create your ROS package (project) that you will use to develop programs.<br> 
▸ the package must be created inside the src folder<br> 
▸ first move to the folder<br> 
▸ cd ~catkin_ws/src/<br>
▸ Create your package (specify the dependencies)<br> 
▸ catkin_create_pkg cs460_package std_msgs rospy roscpp<br> 
▸ Go to catkin_ws and compile<br> 
▸ cd ..<br> 
▸ catkin_make<br> 
▸ this will generate executable and configuration files for the project<br> 

**MAKE THE NEW PACKAGE THE DEFAULT ONE**<br>
▸ add the following command in .bashrc<br> 
▸ source /home/gyan/catkin_ws/devel/setup.bash<br> 
▸ replace gyan by your username<br>


### How to Configure Eclipse to Program with ROS

It shows how to integrate Eclipse IDE in ROS Catkin Workspace. The [ROS IDEs](http://wiki.ros.org/IDEs#Eclipse) page present details for integrating other IDEs. This page provides the simplified steps to configure Eclipse to work with Catkin.

===> **Step 1. Install and Configure Eclipse**
 - First, we need to install Eclipse. Before installation, make sure to install Java Virtual Machine (JVM) because eclipse is programmed with Java. Run the following command:

       sudo apt-get install default-jre

Then, download Eclipse IDE for C/C++. Since/if you use Ubuntu OS, download Linux-32 bits or Linux-64 depending on your operating system.
Extract the downloaded package and move it into */opt* directory with the command

    sudo mv eclipse /opt

As */opt* might need some admin privileges, it might be useful to change previdelged of the eclipse folder to be accessible by any user by doing the following

    cd /opt
    sudo chmod -R 777 eclipse

You can create a link to be used by all users

    sudo ln -s /opt/eclipse/eclipse /usr/bin/eclipse

Then, for easier access, you can add the following text into a unit dash entry:

    sudo gedit /usr/share/applications/eclipse.desktop

and add the following text

    [Desktop Entry]
    Name=Eclipse 
    Type=Application
    Exec=bash -i -c "/opt/eclipse/eclipse"
    Terminal=false
    Icon=/opt/eclipse/icon.xpm 
    Comment=Integrated Development Environment
    NoDisplay=false
    Categories=Development;IDE
    Name[en]=eclipse.desktop

The final step is to compile the project workspace and auto generate eclipse project files:

    $cd ~/catkin_ws
    $catkin_make --force-cmake -G"Eclipse CDT4 - Unix Makefiles"

The project files will be generated in the *build/* folder (*~/catkin_ws/build/.project* and *~/catkin_ws/build/.cproject*)

===> **Step 2. Import the project into Eclipse**

Now, start Eclipse. Choose your *catkin_ws* as the workspace folder.

Then, choose

    File --> Import --> General --> Existing Projects into Workspace

Now import the project from the *~/catkin_ws/build* folder.

**Fix Preprocessor Include Paths**

By default, the intellisense in Eclipse won’t recognize the system header files (like <string>). To fix that: Go to

    Project Properties --> C/C++ General --> Preprocessor Include Paths, Macros, etc. --> Providers tab

Check

    CDT GCC Built-in Compiler Settings

After that rebuild the C/C++ index by Right click on

    project -> Index -> Rebuild


===> **Step 3. Create a ROS Project**

* Eclipse provides a link Source directory within the project so that you can edit the source code.


* Right click on src and select New –> Source File, and create a file named talker.cpp


* Use Eclipse standard shortcuts to get code completion (i.e., Ctrl+Space)


===> **Step 4. Write your first code**

The following code provide simple publisher node that periodically publish a hello message of type std_msgs/String

```C++
#include "ros/ros.h"
#include "std_msgs/String.h"
#include <sstream>

int main(int argc, char **argv)
{
   ros::init(argc, argv, "talker"); // Initiate new ROS node named "talker"

   ros::NodeHandle n;
   ros::Publisher chatter_pub = n.advertise<std_msgs::String>("chatter", 1000);
   ros::Rate loop_rate(10);

   int count = 0;
   while (ros::ok()) // Keep spinning loop until user presses Ctrl+C
   {
       std_msgs::String msg;

       std::stringstream ss;
       ss << "hello world " << count;
       msg.data = ss.str(); 
       ROS_INFO("%s", msg.data.c_str());

       chatter_pub.publish(msg);

       ros::spinOnce(); // Need to call this function often to allow ROS to process incoming messages

      loop_rate.sleep(); // Sleep for the rest of the cycle, to enforce the loop rate
       count++;
   } 
   return 0;
}
```

===> **Step 5. Building your node**

First, you need to modify the *CMakeLists.txt* of your package. The changes you need to make are hilighted in red colour.

    500 

Sometimes, when your node depends on other executable targets, you need to add the appropriate dependencies. For example:

    add_dependencies(talker beginner_tutorials_generate_message_cpp)

This makes sure message headers are generated before being used.
After changing the CMakeLists file call catkin_make

===> **Step 5. Running the Code Inside Eclipse**

* Create a new launch configuration, by clicking on
   
      Run --> Run configurations... --> C/C++ Application (double click or click on New). 
* Select the correct binary on the main tab (use the Browse… button)

      ~/catkin_ws/devel/lib/beginner_tutorials/talker

* Make sure roscore is running in a terminal
* Click Run

      500

Then, you will see the following output

    500

===> **Step 5. Running the Node From a Terminal**

First, make sure you have sourced your workspace

    cd ~/catkin_ws
    source devel/setup.bash

Then, run the node as follows

    rosrun beginner_tutorials talker

You will see the following output

    500


## ROS Ecosystem

![rosecosystem](https://github.com/gyanprakash0221/ROS-for-Beginners-/blob/main/images/rosecosystem.png)
