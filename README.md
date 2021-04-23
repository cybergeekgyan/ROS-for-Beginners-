# ROS-for-Beginners-

### ROS Installation Tips

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
