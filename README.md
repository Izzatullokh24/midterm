# midterm
# Week 1

```
izzatullokh@izzatullokh-virtual-machine:~$ locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings
LANG=en_US.UTF-8
LANGUAGE=
LC_CTYPE="en_US.UTF-8"
LC_NUMERIC="en_US.UTF-8"
LC_TIME="en_US.UTF-8"
LC_COLLATE="en_US.UTF-8"
LC_MONETARY="en_US.UTF-8"
LC_MESSAGES="en_US.UTF-8"
LC_PAPER="en_US.UTF-8"
LC_NAME="en_US.UTF-8"
LC_ADDRESS="en_US.UTF-8"
LC_TELEPHONE="en_US.UTF-8"
LC_MEASUREMENT="en_US.UTF-8"
LC_IDENTIFICATION="en_US.UTF-8"
LC_ALL=en_US.UTF-8
[sudo] password for izzatullokh: 
Get:1 http://packages.ros.org/ros2/ubuntu jammy InRelease [4,673 B]            
Hit:2 http://kr.archive.ubuntu.com/ubuntu jammy InRelease                      
Get:3 http://security.ubuntu.com/ubuntu jammy-security InRelease [110 kB]    
Get:4 http://kr.archive.ubuntu.com/ubuntu jammy-updates InRelease [114 kB]     
Get:5 http://packages.ros.org/ros2/ubuntu jammy/main amd64 Packages [737 kB]   
Get:6 http://kr.archive.ubuntu.com/ubuntu jammy-backports InRelease [99.8 kB]  
Get:7 http://kr.archive.ubuntu.com/ubuntu jammy-updates/main amd64 Packages [655 kB]
Get:8 http://security.ubuntu.com/ubuntu jammy-security/main i386 Packages [141 kB]
Get:9 http://kr.archive.ubuntu.com/ubuntu jammy-updates/main i386 Packages [337 kB]
Get:10 http://kr.archive.ubuntu.com/ubuntu jammy-updates/main Translation-en [150 kB]
Get:11 http://kr.archive.ubuntu.com/ubuntu jammy-updates/main amd64 DEP-11 Metadata [92.8 kB]
Get:12 http://kr.archive.ubuntu.com/ubuntu jammy-updates/main amd64 c-n-f Metadata [9,100 B]
Get:13 http://kr.archive.ubuntu.com/ubuntu jammy-updates/restricted amd64 Packages [399 kB]
Get:14 http://security.ubuntu.com/ubuntu jammy-security/main amd64 Packages [375 kB]
Get:15 http://kr.archive.ubuntu.com/ubuntu jammy-updates/restricted i386 Packages [22.1 kB]
Get:16 http://kr.archive.ubuntu.com/ubuntu jammy-updates/restricted Translation-en [61.3 kB]
Get:17 http://kr.archive.ubuntu.com/ubuntu jammy-updates/restricted amd64 c-n-f Metadata [532 B]
Get:18 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe i386 Packages [281 kB]
Get:19 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 Packages [433 kB]
Get:20 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe Translation-en [109 kB]
Get:21 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 DEP-11 Metadata [248 kB]
Get:22 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe DEP-11 48x48 Icons [156 kB]
Get:23 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe DEP-11 64x64 Icons [234 kB]
Get:24 http://kr.archive.ubuntu.com/ubuntu jammy-updates/multiverse amd64 DEP-11 Metadata [940 B]
Get:25 http://kr.archive.ubuntu.com/ubuntu jammy-backports/universe amd64 Packages [6,752 B]
Get:26 http://kr.archive.ubuntu.com/ubuntu jammy-backports/universe i386 Packages [5,200 B]
Get:27 http://kr.archive.ubuntu.com/ubuntu jammy-backports/universe amd64 DEP-11 Metadata [12.5 kB]
Get:28 http://kr.archive.ubuntu.com/ubuntu jammy-backports/universe amd64 c-n-f Metadata [352 B]
Get:29 http://security.ubuntu.com/ubuntu jammy-security/main Translation-en [85.4 kB]
Get:30 http://security.ubuntu.com/ubuntu jammy-security/main amd64 DEP-11 Metadata [13.0 kB]
Get:31 http://security.ubuntu.com/ubuntu jammy-security/restricted amd64 Packages [339 kB]
Get:32 http://security.ubuntu.com/ubuntu jammy-security/restricted i386 Packages [21.8 kB]
Get:33 http://security.ubuntu.com/ubuntu jammy-security/restricted Translation-en [52.2 kB]
Get:34 http://security.ubuntu.com/ubuntu jammy-security/universe amd64 Packages [293 kB]
Get:35 http://security.ubuntu.com/ubuntu jammy-security/universe i386 Packages [211 kB]
Get:36 http://security.ubuntu.com/ubuntu jammy-security/universe Translation-en [64.4 kB]
Get:37 http://security.ubuntu.com/ubuntu jammy-security/universe amd64 DEP-11 Metadata [12.4 kB]
Get:38 http://security.ubuntu.com/ubuntu jammy-security/universe DEP-11 64x64 Icons [9,532 B]
Fetched 5,898 kB in 42s (142 kB/s)                                             
  

```

# Ros 2 Apt repository

```
izzatullokh@izzatullokh-virtual-machine:~$ apt-cache policy | grep universe
 500 http://security.ubuntu.com/ubuntu jammy-security/universe i386 Packages
     release v=22.04,o=Ubuntu,a=jammy-security,n=jammy,l=Ubuntu,c=universe,b=i386
 500 http://security.ubuntu.com/ubuntu jammy-security/universe amd64 Packages
     release v=22.04,o=Ubuntu,a=jammy-security,n=jammy,l=Ubuntu,c=universe,b=amd64
 100 http://kr.archive.ubuntu.com/ubuntu jammy-backports/universe i386 Packages
     release v=22.04,o=Ubuntu,a=jammy-backports,n=jammy,l=Ubuntu,c=universe,b=i386
 100 http://kr.archive.ubuntu.com/ubuntu jammy-backports/universe amd64 Packages
     release v=22.04,o=Ubuntu,a=jammy-backports,n=jammy,l=Ubuntu,c=universe,b=amd64
 500 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe i386 Packages
     release v=22.04,o=Ubuntu,a=jammy-updates,n=jammy,l=Ubuntu,c=universe,b=i386
 500 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 Packages
     release v=22.04,o=Ubuntu,a=jammy-updates,n=jammy,l=Ubuntu,c=universe,b=amd64
 500 http://kr.archive.ubuntu.com/ubuntu jammy/universe i386 Packages
     release v=22.04,o=Ubuntu,a=jammy,n=jammy,l=Ubuntu,c=universe,b=i386
 500 http://kr.archive.ubuntu.com/ubuntu jammy/universe amd64 Packages
     release v=22.04,o=Ubuntu,a=jammy,n=jammy,l=Ubuntu,c=universe,b=amd64
izzatullokh@izzatullokh-virtual-machine:~$ 

```
## Now add the ROS 2 apt repository to your system. First authorize our GPG key with apt.
```
izzatullokh@izzatullokh-virtual-machine:~$ sudo apt update && sudo apt install curl gnupg lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
Reading package lists... Done
E: Could not get lock /var/lib/apt/lists/lock. It is held by process 6991 (aptd)
N: Be aware that removing the lock file is not a solution and may break your system.
E: Unable to lock directory /var/lib/apt/lists/
izzatullokh@izzatullokh-virtual-machine:~$ 
```
## Then add the repository to your sources list.
```
izzatullokh@izzatullokh-virtual-machine:~$ echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
izzatullokh@izzatullokh-virtual-machine:~$ 

```

# Install development tools and ROS tools
## Install common packages

```
izzatullokh@izzatullokh-virtual-machine:~$ sudo apt update && sudo apt install -y \
  build-essential \
  cmake \
  git \
  python3-colcon-common-extensions \
  python3-flake8 \
  python3-flake8-docstrings \
  python3-pip \
  python3-pytest \
  python3-pytest-cov \
  python3-rosdep \
  python3-setuptools \
  python3-vcstool \
  wget
Reading package lists... Done
E: Could not get lock /var/lib/apt/lists/lock. It is held by process 6991 (aptd)
N: Be aware that removing the lock file is not a solution and may break your system.
E: Unable to lock directory /var/lib/apt/lists/
izzatullokh@izzatullokh-virtual-machine:~$ 

```
## Install packages according to our Ubuntu version
### Install dependencies using rosdep 
```
izzatullokh@izzatullokh-virtual-machine:~/ros2_humble$ sudo rosdep init
rosdep update
rosdep install --from-paths src --ignore-src -y --skip-keys "fastcdr rti-connext-dds-6.0.1 urdfdom_headers"
ERROR: default sources list file already exists:
	/etc/ros/rosdep/sources.list.d/20-default.list
Please delete if you wish to re-initialize
reading in sources list data from /etc/ros/rosdep/sources.list.d
ERROR: unable to process source [file:///usr/share/python3-rosdep2/debian.yaml]:
	<urlopen error [Errno 2] No such file or directory: '/usr/share/python3-rosdep2/debian.yaml'> (file:///usr/share/python3-rosdep2/debian.yaml)
Hit https://raw.githubusercontent.com/ros/rosdistro/master/rosdep/osx-homebrew.yaml
Hit https://raw.githubusercontent.com/ros/rosdistro/master/rosdep/base.yaml
Hit https://raw.githubusercontent.com/ros/rosdistro/master/rosdep/python.yaml
Hit https://raw.githubusercontent.com/ros/rosdistro/master/rosdep/ruby.yaml
Hit https://raw.githubusercontent.com/ros/rosdistro/master/releases/fuerte.yaml
Query rosdistro index https://raw.githubusercontent.com/ros/rosdistro/master/index-v4.yaml
Skip end-of-life distro "ardent"
Skip end-of-life distro "bouncy"
Skip end-of-life distro "crystal"
Skip end-of-life distro "dashing"
Skip end-of-life distro "eloquent"
Add distro "foxy"
Add distro "galactic"
Skip end-of-life distro "groovy"
Add distro "humble"
Skip end-of-life distro "hydro"
Skip end-of-life distro "indigo"
Skip end-of-life distro "jade"
Skip end-of-life distro "kinetic"
Skip end-of-life distro "lunar"
Add distro "melodic"
Add distro "noetic"
Add distro "rolling"
updated cache in /home/izzatullokh/.ros/rosdep/sources.cache
ERROR: Not all sources were able to be updated.
[[[
ERROR: unable to process source [file:///usr/share/python3-rosdep2/debian.yaml]:
	<urlopen error [Errno 2] No such file or directory: '/usr/share/python3-rosdep2/debian.yaml'> (file:///usr/share/python3-rosdep2/debian.yaml)
]]]
WARNING: ROS_PYTHON_VERSION is unset. Defaulting to 3
#All required rosdeps installed successfully
```
# week 4
## source the set up files
```
izzatullokh@izzatullokh-virtual-machine:~/ros2_humble$ # Replace ".bash" with your shell if you're not using bash
# Possible values are: setup.bash, setup.sh, setup.zsh
source /opt/ros/humble/setup.bash
izzatullokh@izzatullokh-virtual-machine:~/ros2_humble$ 


```
## 1 Install turtlesim
### Install the turtlesim package for our ROS 2 distro:
```
izzatullokh@izzatullokh-virtual-machine:~$ # Replace ".bash" with your shell if you're not using bash
# Possible values are: setup.bash, setup.sh, setup.zsh
source /opt/ros/humble/setup.bash
izzatullokh@izzatullokh-virtual-machine:~$ sudo apt update

sudo apt install ros-humble-turtlesim
[sudo] password for izzatullokh: 
Hit:1 http://packages.ros.org/ros2/ubuntu jammy InRelease
Get:2 http://security.ubuntu.com/ubuntu jammy-security InRelease [110 kB]
Hit:3 http://kr.archive.ubuntu.com/ubuntu jammy InRelease
Get:4 http://kr.archive.ubuntu.com/ubuntu jammy-updates InRelease [114 kB]
Get:5 http://security.ubuntu.com/ubuntu jammy-security/main amd64 DEP-11 Metadata [13.0 kB]
Get:6 http://security.ubuntu.com/ubuntu jammy-security/universe amd64 DEP-11 Metadata [12.4 kB]
Get:7 http://kr.archive.ubuntu.com/ubuntu jammy-backports InRelease [99.8 kB]
Get:8 http://kr.archive.ubuntu.com/ubuntu jammy-updates/main amd64 Packages [655 kB]
Get:9 http://kr.archive.ubuntu.com/ubuntu jammy-updates/main i386 Packages [337 kB]
Get:10 http://kr.archive.ubuntu.com/ubuntu jammy-updates/main amd64 DEP-11 Metadata [92.8 kB]                                                       
Get:11 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 Packages [434 kB]                                                           
Get:12 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe i386 Packages [281 kB]                                                            
Get:13 http://kr.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 DEP-11 Metadata [248 kB]                                                    
Get:14 http://kr.archive.ubuntu.com/ubuntu jammy-updates/multiverse amd64 DEP-11 Metadata [940 B]                                                   
Get:15 http://kr.archive.ubuntu.com/ubuntu jammy-backports/universe amd64 DEP-11 Metadata [12.6 kB]                                                 
Fetched 2,411 kB in 11s (213 kB/s)                                                                                                                  
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
140 packages can be upgraded. Run 'apt list --upgradable' to see them.
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
ros-humble-turtlesim is already the newest version (1.4.2-1jammy.20220908.233909).
The following packages were automatically installed and are no longer required:
  python3-catkin-pkg python3-rosdistro
Use 'sudo apt autoremove' to remove them.
0 upgraded, 0 newly installed, 0 to remove and 140 not upgraded.
```
## Checking that the package installed:
```
izzatullokh@izzatullokh-virtual-machine:~$ ros2 pkg executables turtlesim
turtlesim draw_square
turtlesim mimic
turtlesim turtle_teleop_key
turtlesim turtlesim_node
izzatullokh@izzatullokh-virtual-machine:~$
```
# Start turtelism
```
izzatullokh@izzatullokh-virtual-machine:~$ ros2 run turtlesim turtlesim_node
Warning: Ignoring XDG_SESSION_TYPE=wayland on Gnome. Use QT_QPA_PLATFORM=wayland to run on Wayland anyway.
[INFO] [1666155565.273879580] [turtlesim]: Starting turtlesim with node name /turtlesim
[INFO] [1666155565.316003811] [turtlesim]: Spawning turtle [turtle1] at x=[5.544445], y=[5.544445], theta=[0.000000]

```
![Screenshot from 2022-10-19 14-00-50](https://user-images.githubusercontent.com/86156093/196601838-59e21d0d-8b7b-4f94-a182-244c0538d2f0.png)

## Open a new terminal and source ROS 2 again.
```
izzatullokh@izzatullokh-virtual-machine:~$ source /opt/ros/humble/setup.bash
izzatullokh@izzatullokh-virtual-machine:~$ ros2 run turtlesim turtle_teleop_key
Reading from keyboard
---------------------------
Use arrow keys to move the turtle.
Use G|B|V|C|D|E|R|T keys to rotate to absolute orientations. 'F' to cancel a rotation.
'Q' to quit.



```
# Install rqt
## open a new terminal and try following code 


```
izzatullokh@izzatullokh-virtual-machine:~$ sudo apt update

sudo apt install ~nros-humble-rqt*
[sudo] password for izzatullokh: 
Hit:1 http://packages.ros.org/ros2/ubuntu jammy InRelease                      
Hit:2 http://kr.archive.ubuntu.com/ubuntu jammy InRelease                      
Hit:3 http://security.ubuntu.com/ubuntu jammy-security InRelease               
Hit:4 http://kr.archive.ubuntu.com/ubuntu jammy-updates InRelease
Hit:5 http://kr.archive.ubuntu.com/ubuntu jammy-backports InRelease
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
140 packages can be upgraded. Run 'apt list --upgradable' to see them.
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
ros-humble-rqt is already the newest version (1.1.4-1jammy.20220909.020555).
ros-humble-rqt-bag is already the newest version (1.1.3-2jammy.20220909.040110).
ros-humble-rqt-bag-plugins is already the newest version (1.1.3-2jammy.20220909.041037).
ros-humble-rqt-console is already the newest version (2.0.2-3jammy.20220909.015543).
ros-humble-rqt-gui is already the newest version (1.1.4-1jammy.20220908.195723).
ros-humble-rqt-gui-cpp is already the newest version (1.1.4-1jammy.20220908.231335).
ros-humble-rqt-gui-cpp-dbgsym is already the newest version (1.1.4-1jammy.20220908.231335).
ros-humble-rqt-gui-py is already the newest version (1.1.4-1jammy.20220909.014649).
ros-humble-rqt-image-overlay-layer is already the newest version (0.1.1-1jammy.20220908.231412).
ros-humble-rqt-plot is already the newest version (1.1.2-1jammy.20220909.015608).
ros-humble-rqt-publisher is already the newest version (1.5.0-1jammy.20220909.020605).
ros-humble-rqt-py-common is already the newest version (1.1.4-1jammy.20220908.195729).
ros-humble-rqt-py-console is already the newest version (1.0.2-3jammy.20220909.015615).
ros-humble-rqt-robot-dashboard is already the newest version (0.6.1-3jammy.20220909.020338).
ros-humble-rqt-robot-monitor is already the newest version (1.0.5-2jammy.20220909.015649).
ros-humble-rqt-robot-steering is already the newest version (1.0.0-4jammy.20220909.015758).
ros-humble-rqt-runtime-monitor is already the newest version (1.0.0-3jammy.20220909.015906).
ros-humble-rqt-service-caller is already the newest version (1.0.5-3jammy.20220909.020607).
ros-humble-rqt-shell is already the newest version (1.0.2-3jammy.20220909.020610).
The following packages were automatically installed and are no longer required:
  python3-catkin-pkg python3-rosdistro
Use 'sudo apt autoremove' to remove them.
The following packages will be upgraded:
  ros-humble-rqt-action ros-humble-rqt-common-plugins ros-humble-rqt-graph
  ros-humble-rqt-image-overlay ros-humble-rqt-image-overlay-dbgsym
  ros-humble-rqt-image-view ros-humble-rqt-image-view-dbgsym
  ros-humble-rqt-joint-trajectory-controller ros-humble-rqt-moveit
  ros-humble-rqt-msg ros-humble-rqt-reconfigure ros-humble-rqt-srv
  ros-humble-rqt-tf-tree ros-humble-rqt-topic
14 upgraded, 0 newly installed, 0 to remove and 126 not upgraded.
Need to get 0 B/6,580 kB of archives.
After this operation, 1,024 B of additional disk space will be used.
Do you want to continue? [Y/n] y
(Reading database ... 291246 files and directories currently installed.)
Preparing to unpack .../00-ros-humble-rqt-msg_1.2.0-1jammy.20220913.193603_amd64
.deb ...
Unpacking ros-humble-rqt-msg (1.2.0-1jammy.20220913.193603) over (1.0.6-2jammy.2
0220909.020245) ...
Preparing to unpack .../01-ros-humble-rqt-action_2.0.1-3jammy.20220913.193725_am
d64.deb ...
Unpacking ros-humble-rqt-action (2.0.1-3jammy.20220913.193725) over (2.0.1-3jamm
y.20220909.020558) ...
Preparing to unpack .../02-ros-humble-rqt-graph_1.3.0-1jammy.20220914.011333_amd
64.deb ...
Unpacking ros-humble-rqt-graph (1.3.0-1jammy.20220914.011333) over (1.2.1-3jammy
.20220909.020555) ...
Preparing to unpack .../03-ros-humble-rqt-image-view-dbgsym_1.2.0-2jammy.2022092
2.180454_amd64.deb ...
Unpacking ros-humble-rqt-image-view-dbgsym (1.2.0-2jammy.20220922.180454) over (
1.2.0-2jammy.20220908.232521) ...
Preparing to unpack .../04-ros-humble-rqt-image-view_1.2.0-2jammy.20220922.18045
4_amd64.deb ...
Unpacking ros-humble-rqt-image-view (1.2.0-2jammy.20220922.180454) over (1.2.0-2
jammy.20220908.232521) ...
Preparing to unpack .../05-ros-humble-rqt-reconfigure_1.1.1-1jammy.20220913.2220
47_amd64.deb ...
Unpacking ros-humble-rqt-reconfigure (1.1.1-1jammy.20220913.222047) over (1.0.8-
3jammy.20220909.020245) ...
Preparing to unpack .../06-ros-humble-rqt-srv_1.0.3-3jammy.20220913.193724_amd64
.deb ...
Unpacking ros-humble-rqt-srv (1.0.3-3jammy.20220913.193724) over (1.0.3-3jammy.2
0220909.020558) ...
Preparing to unpack .../07-ros-humble-rqt-topic_1.5.0-1jammy.20220913.192543_amd
64.deb ...
Unpacking ros-humble-rqt-topic (1.5.0-1jammy.20220913.192543) over (1.2.3-2jammy
.20220909.020611) ...
Preparing to unpack .../08-ros-humble-rqt-common-plugins_1.2.0-1jammy.20220922.1
85410_amd64.deb ...
Unpacking ros-humble-rqt-common-plugins (1.2.0-1jammy.20220922.185410) over (1.2
.0-1jammy.20220909.041109) ...
Preparing to unpack .../09-ros-humble-rqt-image-overlay-dbgsym_0.1.1-1jammy.2022
0922.185333_amd64.deb ...
Unpacking ros-humble-rqt-image-overlay-dbgsym (0.1.1-1jammy.20220922.185333) ove
r (0.1.1-1jammy.20220909.023022) ...
Preparing to unpack .../10-ros-humble-rqt-image-overlay_0.1.1-1jammy.20220922.18
5333_amd64.deb ...
Unpacking ros-humble-rqt-image-overlay (0.1.1-1jammy.20220922.185333) over (0.1.
1-1jammy.20220909.023022) ...
Preparing to unpack .../11-ros-humble-rqt-joint-trajectory-controller_2.12.0-1ja
mmy.20220919.173818_amd64.deb ...
Unpacking ros-humble-rqt-joint-trajectory-controller (2.12.0-1jammy.20220919.173
818) over (2.12.0-1jammy.20220909.015543) ...
Preparing to unpack .../12-ros-humble-rqt-moveit_1.0.1-3jammy.20220913.192707_am
d64.deb ...
Unpacking ros-humble-rqt-moveit (1.0.1-3jammy.20220913.192707) over (1.0.1-3jamm
y.20220909.020717) ...
Preparing to unpack .../13-ros-humble-rqt-tf-tree_1.0.4-1jammy.20220914.011613_a
md64.deb ...
Unpacking ros-humble-rqt-tf-tree (1.0.4-1jammy.20220914.011613) over (1.0.4-1jam
my.20220909.020623) ...
Setting up ros-humble-rqt-topic (1.5.0-1jammy.20220913.192543) ...
Setting up ros-humble-rqt-graph (1.3.0-1jammy.20220914.011333) ...
Setting up ros-humble-rqt-image-overlay (0.1.1-1jammy.20220922.185333) ...
Setting up ros-humble-rqt-reconfigure (1.1.1-1jammy.20220913.222047) ...
Setting up ros-humble-rqt-tf-tree (1.0.4-1jammy.20220914.011613) ...
Setting up ros-humble-rqt-joint-trajectory-controller (2.12.0-1jammy.20220919.17
3818) ...
Setting up ros-humble-rqt-moveit (1.0.1-3jammy.20220913.192707) ...
Setting up ros-humble-rqt-image-view (1.2.0-2jammy.20220922.180454) ...
Setting up ros-humble-rqt-image-overlay-dbgsym (0.1.1-1jammy.20220922.185333) ..
.
Setting up ros-humble-rqt-msg (1.2.0-1jammy.20220913.193603) ...
Setting up ros-humble-rqt-srv (1.0.3-3jammy.20220913.193724) ...
Setting up ros-humble-rqt-image-view-dbgsym (1.2.0-2jammy.20220922.180454) ...
Setting up ros-humble-rqt-action (2.0.1-3jammy.20220913.193725) ...
Setting up ros-humble-rqt-common-plugins (1.2.0-1jammy.20220922.185410) ...
izzatullokh@izzatullokh-virtual-machine:~$ 



```
## run the rqt 
```

izzatullokh@izzatullokh-virtual-machine:~$ rqt

```
![Screenshot from 2022-10-19 14-13-33](https://user-images.githubusercontent.com/86156093/196603292-1b7b9227-9c6f-471f-af44-50b153df3f0c.png)

## Try the spawn service

![Screenshot from 2022-10-19 14-18-15](https://user-images.githubusercontent.com/86156093/196603597-c8dc0ccc-d710-412c-971d-cbdc01386b5d.png)
## Remapping

```
izzatullokh@izzatullokh-virtual-machine:~$ source /opt/ros/humble/setup.bash
izzatullokh@izzatullokh-virtual-machine:~$ ros2 run turtlesim turtle_teleop_key --ros-args --remap turtle1/cmd_vel:=turtle2/cmd_vel
Reading from keyboard
---------------------------
Use arrow keys to move the turtle.
Use G|B|V|C|D|E|R|T keys to rotate to absolute orientations. 'F' to cancel a rotation.
'Q' to quit.




# Install Colcon

instaling colcon by entering following commands:
```
sudo apt install python3-colcon-common-extensions
```
```
izzatullokh@izzatullokh-virtual-machine:~$ sudo apt install python3-colcon-common-extensions
[sudo] password for izzatullokh: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
python3-colcon-common-extensions is already the newest version (0.3.0-1).
The following packages were automatically installed and are no longer required:
  python3-catkin-pkg python3-rosdistro
Use 'sudo apt autoremove' to remove them.
0 upgraded, 0 newly installed, 0 to remove and 126 not upgraded.
izzatullokh@izzatullokh-virtual-machine:~$ 
```
## Creating a workspace and add some source to it:
```

izzatullokh@izzatullokh-virtual-machine:~$ mkdir -p ~/ros2_ws/src
cd ~/ros2_ws
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ .
└── src

1 directory, 0 files
bash: .: filename argument required
.: usage: . filename [arguments]
└──: command not found
1: command not found
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ git clone https://github.com/ros2/examples src/examples -b humble
fatal: destination path 'src/examples' already exists and is not an empty directory.
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ # Replace ".bash" with your shell if you're not using bash
# Possible values are: setup.bash, setup.sh, setup.zsh
source /opt/ros/humble/setup.bash
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ git clone https://github.com/ros2/examples src/examples -b humble
fatal: destination path 'src/examples' already exists and is not an empty directory.
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ 
```

## Building a workspace
```
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ colcon build --symlink-install
[3.312s] WARNING:colcon.colcon_core.package_selection:Some selected packages are already built in one or more underlay workspaces:
	'examples_rclcpp_minimal_action_client' is in: /opt/ros/humble
	'examples_rclcpp_minimal_timer' is in: /opt/ros/humble
	'examples_rclcpp_minimal_composition' is in: /opt/ros/humble
	'examples_rclcpp_minimal_subscriber' is in: /opt/ros/humble
	'turtlesim' is in: /opt/ros/humble
	'action_tutorials_interfaces' is in: /opt/ros/humble
	'examples_rclcpp_minimal_client' is in: /opt/ros/humble
	'examples_rclcpp_minimal_service' is in: /opt/ros/humble
	'examples_rclcpp_multithreaded_executor' is in: /opt/ros/humble
	'examples_rclpy_executors' is in: /opt/ros/humble
	'examples_rclcpp_minimal_publisher' is in: /opt/ros/humble
	'examples_rclpy_minimal_service' is in: /opt/ros/humble
	'examples_rclcpp_minimal_action_server' is in: /opt/ros/humble
	'examples_rclpy_minimal_subscriber' is in: /opt/ros/humble
	'examples_rclpy_minimal_action_server' is in: /opt/ros/humble
	'examples_rclpy_minimal_publisher' is in: /opt/ros/humble
	'examples_rclpy_minimal_action_client' is in: /opt/ros/humble
	'examples_rclpy_minimal_client' is in: /opt/ros/humble
If a package in a merged underlay workspace is overridden and it installs headers, then all packages in the overlay must sort their include directories by workspace order. Failure to do so may result in build failures or undefined behavior at run time.
If the overridden package is used by another package in any underlay, then the overriding package in the overlay must be API and ABI compatible or undefined behavior at run time may occur.

If you understand the risks and want to override a package anyways, add the following to the command line:
	--allow-overriding action_tutorials_interfaces examples_rclcpp_minimal_action_client examples_rclcpp_minimal_action_server examples_rclcpp_minimal_client examples_rclcpp_minimal_composition examples_rclcpp_minimal_publisher examples_rclcpp_minimal_service examples_rclcpp_minimal_subscriber examples_rclcpp_minimal_timer examples_rclcpp_multithreaded_executor examples_rclpy_executors examples_rclpy_minimal_action_client examples_rclpy_minimal_action_server examples_rclpy_minimal_client examples_rclpy_minimal_publisher examples_rclpy_minimal_service examples_rclpy_minimal_subscriber turtlesim

This may be promoted to an error in a future release of colcon-override-check.
Starting >>> action_tutorials_interfaces
Starting >>> examples_rclcpp_async_client
--- stderr: action_tutorials_interfaces                                    
CMake Error at /opt/ros/humble/share/rosidl_cmake/cmake/rosidl_generate_interfaces.cmake:93 (message):
  rosidl_generate_interfaces() the passed file 'action/Fibonacci.action'
  doesn't exist relative to the CMAKE_CURRENT_SOURCE_DIR
  '/home/izzatullokh/ros2_ws/src/ros2_ws/src/action_tutorials_interfaces'
Call Stack (most recent call first):
  CMakeLists.txt:28 (rosidl_generate_interfaces)


---
Failed   <<< action_tutorials_interfaces [4.19s, exited with code 1]
Aborted  <<< examples_rclcpp_async_client [4.80s]                            

Summary: 0 packages finished [6.30s]
  1 package failed: action_tutorials_interfaces
  1 package aborted: examples_rclcpp_async_client
  1 package had stderr output: action_tutorials_interfaces
  25 packages not processed
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ 
```
## Run tests
### To run tests for the packages we just built, run the following:
```
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ colcon test
Starting >>> action_tutorials_interfaces
Starting >>> examples_rclcpp_async_client
Finished <<< action_tutorials_interfaces [0.20s]                           
Starting >>> examples_rclcpp_cbg_executor
Finished <<< examples_rclcpp_cbg_executor [9.29s]                            
Starting >>> examples_rclcpp_minimal_action_client
Finished <<< examples_rclcpp_async_client [9.47s]                            
Starting >>> examples_rclcpp_minimal_action_server
Finished <<< examples_rclcpp_minimal_action_server [5.36s]
Starting >>> examples_rclcpp_minimal_client
Finished <<< examples_rclcpp_minimal_action_client [5.63s]
Starting >>> examples_rclcpp_minimal_composition
Finished <<< examples_rclcpp_minimal_client [5.07s]                            
Starting >>> examples_rclcpp_minimal_publisher
Finished <<< examples_rclcpp_minimal_composition [6.16s]
Starting >>> examples_rclcpp_minimal_service
Finished <<< examples_rclcpp_minimal_publisher [6.10s]
Starting >>> examples_rclcpp_minimal_subscriber
Finished <<< examples_rclcpp_minimal_service [5.01s]
Starting >>> examples_rclcpp_minimal_timer
Finished <<< examples_rclcpp_minimal_timer [9.49s]
Starting >>> examples_rclcpp_multithreaded_executor
Finished <<< examples_rclcpp_minimal_subscriber [9.85s]
Starting >>> examples_rclcpp_wait_set
Finished <<< examples_rclcpp_multithreaded_executor [5.18s]
Starting >>> examples_rclpy_executors
Finished <<< examples_rclcpp_wait_set [8.02s]                             
Starting >>> examples_rclpy_guard_conditions
--- stderr: examples_rclpy_executors                                      

=============================== warnings summary ===============================
executors/test/test_flake8.py::test_flake8
executors/test/test_flake8.py::test_flake8
  Warning: SelectableGroups dict interface is deprecated. Use select.

-- Docs: https://docs.pytest.org/en/stable/warnings.html
---
Finished <<< examples_rclpy_executors [6.77s]
Starting >>> examples_rclpy_minimal_action_client
--- stderr: examples_rclpy_guard_conditions

=============================== warnings summary ===============================
guard_conditions/test/test_flake8.py::test_flake8
guard_conditions/test/test_flake8.py::test_flake8
  Warning: SelectableGroups dict interface is deprecated. Use select.

-- Docs: https://docs.pytest.org/en/stable/warnings.html
---
Finished <<< examples_rclpy_guard_conditions [4.99s]
Starting >>> examples_rclpy_minimal_action_server
--- stderr: examples_rclpy_minimal_action_client

=============================== warnings summary ===============================
actions/minimal_action_client/test/test_flake8.py::test_flake8
actions/minimal_action_client/test/test_flake8.py::test_flake8
  Warning: SelectableGroups dict interface is deprecated. Use select.

-- Docs: https://docs.pytest.org/en/stable/warnings.html
---
Finished <<< examples_rclpy_minimal_action_client [4.77s]
Starting >>> examples_rclpy_minimal_client
--- stderr: examples_rclpy_minimal_action_server

=============================== warnings summary ===============================
actions/minimal_action_server/test/test_flake8.py::test_flake8
actions/minimal_action_server/test/test_flake8.py::test_flake8
  Warning: SelectableGroups dict interface is deprecated. Use select.

-- Docs: https://docs.pytest.org/en/stable/warnings.html
---
Finished <<< examples_rclpy_minimal_action_server [5.30s]
Starting >>> examples_rclpy_minimal_publisher
--- stderr: examples_rclpy_minimal_client                                      

=============================== warnings summary ===============================
services/minimal_client/test/test_flake8.py::test_flake8
services/minimal_client/test/test_flake8.py::test_flake8
  Warning: SelectableGroups dict interface is deprecated. Use select.

-- Docs: https://docs.pytest.org/en/stable/warnings.html
---
Finished <<< examples_rclpy_minimal_client [5.09s]
Starting >>> examples_rclpy_minimal_service
--- stderr: examples_rclpy_minimal_publisher

=============================== warnings summary ===============================
topics/minimal_publisher/test/test_flake8.py::test_flake8
topics/minimal_publisher/test/test_flake8.py::test_flake8
  Warning: SelectableGroups dict interface is deprecated. Use select.

-- Docs: https://docs.pytest.org/en/stable/warnings.html
---
Finished <<< examples_rclpy_minimal_publisher [4.84s]
Starting >>> examples_rclpy_minimal_subscriber
--- stderr: examples_rclpy_minimal_service  

=============================== warnings summary ===============================
services/minimal_service/test/test_flake8.py::test_flake8
services/minimal_service/test/test_flake8.py::test_flake8
  Warning: SelectableGroups dict interface is deprecated. Use select.

-- Docs: https://docs.pytest.org/en/stable/warnings.html
---
Finished <<< examples_rclpy_minimal_service [4.66s]
Starting >>> examples_rclpy_pointcloud_publisher
--- stderr: examples_rclpy_minimal_subscriber

=============================== warnings summary ===============================
topics/minimal_subscriber/test/test_flake8.py::test_flake8
topics/minimal_subscriber/test/test_flake8.py::test_flake8
  Warning: SelectableGroups dict interface is deprecated. Use select.

-- Docs: https://docs.pytest.org/en/stable/warnings.html
---
Finished <<< examples_rclpy_minimal_subscriber [5.05s]
Starting >>> launch_testing_examples
--- stderr: examples_rclpy_pointcloud_publisher

=============================== warnings summary ===============================
topics/pointcloud_publisher/test/test_flake8.py::test_flake8
topics/pointcloud_publisher/test/test_flake8.py::test_flake8
  Warning: SelectableGroups dict interface is deprecated. Use select.

-- Docs: https://docs.pytest.org/en/stable/warnings.html
---
Finished <<< examples_rclpy_pointcloud_publisher [4.68s]
Starting >>> my_package
Finished <<< my_package [3.05s]                                               
Starting >>> su_bpublisher
Finished <<< su_bpublisher [1.91s]                                            
Starting >>> sub_publisher
Finished <<< sub_publisher [1.60s]                                            
Starting >>> turtlesim
Finished <<< turtlesim [0.12s]                                                
--- stderr: launch_testing_examples                            

=============================== warnings summary ===============================
launch_testing_examples/check_msgs_launch_test.py: 2 warnings
launch_testing_examples/check_multiple_nodes_launch_test.py: 2 warnings
launch_testing_examples/check_node_launch_test.py: 2 warnings
launch_testing_examples/hello_world_launch_test.py: 2 warnings
launch_testing_examples/record_rosbag_launch_test.py: 2 warnings
launch_testing_examples/set_param_launch_test.py: 2 warnings
  Warning: There is no current event loop

test/test_flake8.py::test_flake8
test/test_flake8.py::test_flake8
  Warning: SelectableGroups dict interface is deprecated. Use select.

-- Docs: https://docs.pytest.org/en/stable/warnings.html
---
Finished <<< launch_testing_examples [22.9s]

Summary: 27 packages finished [1min 28s]
  10 packages had stderr output: examples_rclpy_executors examples_rclpy_guard_conditions examples_rclpy_minimal_action_client examples_rclpy_minimal_action_server examples_rclpy_minimal_client examples_rclpy_minimal_publisher examples_rclpy_minimal_service examples_rclpy_minimal_subscriber examples_rclpy_pointcloud_publisher launch_testing_examples
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ 
```
## Source the enviroment
````
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ . install/setup.bash
```
## try a demo
```
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ ros2 run examples_rclcpp_minimal_subscriber subscriber_member_function
[INFO] [1666157611.373149077] [minimal_subscriber]: I heard: 'Hello, world! 0'
[INFO] [1666157611.873090136] [minimal_subscriber]: I heard: 'Hello, world! 1'
[INFO] [1666157612.372648937] [minimal_subscriber]: I heard: 'Hello, world! 2'
[INFO] [1666157612.872870650] [minimal_subscriber]: I heard: 'Hello, world! 3'
[INFO] [1666157613.372911812] [minimal_subscriber]: I heard: 'Hello, world! 4'
[INFO] [1666157613.872663704] [minimal_subscriber]: I heard: 'Hello, world! 5'
[INFO] [1666157614.372776682] [minimal_subscriber]: I heard: 'Hello, world! 6'
[INFO] [1666157614.873356239] [minimal_subscriber]: I heard: 'Hello, world! 7'
[INFO] [1666157615.372547656] [minimal_subscriber]: I heard: 'Hello, world! 8'
[INFO] [1666157615.872023073] [minimal_subscriber]: I heard: 'Hello, world! 9'
[INFO] [1666157616.372481294] [minimal_subscriber]: I heard: 'Hello, world! 10'
[INFO] [1666157616.872645945] [minimal_subscriber]: I heard: 'Hello, world! 11'
[INFO] [1666157617.372732030] [minimal_subscriber]: I heard: 'Hello, world! 12'
[INFO] [1666157617.872892064] [minimal_subscriber]: I heard: 'Hello, world! 13'
[INFO] [1666157618.372756344] [minimal_subscriber]: I heard: 'Hello, world! 14'
[INFO] [1666157618.873561904] [minimal_subscriber]: I heard: 'Hello, world! 15'
[INFO] [1666157619.373497794] [minimal_subscriber]: I heard: 'Hello, world! 16'
[INFO] [1666157619.873019097] [minimal_subscriber]: I heard: 'Hello, world! 17'
[INFO] [1666157620.372486344] [minimal_subscriber]: I heard: 'Hello, world! 18'
[INFO] [1666157620.872930027] [minimal_subscriber]: I heard: 'Hello, world! 19'
[INFO] [1666157621.373231543] [minimal_subscriber]: I heard: 'Hello, world! 20'
[INFO] [1666157621.871991429] [minimal_subscriber]: I heard: 'Hello, world! 21'
[INFO] [1666157622.371825923] [minimal_subscriber]: I heard: 'Hello, world! 22'
[INFO] [1666157622.872768855] [minimal_subscriber]: I heard: 'Hello, world! 23'
[INFO] [1666157623.371765754] [minimal_subscriber]: I heard: 'Hello, world! 24'
[INFO] [1666157623.871812144] [minimal_subscriber]: I heard: 'Hello, world! 25'
[INFO] [1666157624.373643616] [minimal_subscriber]: I heard: 'Hello, world! 26'
[INFO] [1666157624.873041124] [minimal_subscriber]: I heard: 'Hello, world! 27'
[INFO] [1666157625.373254026] [minimal_subscriber]: I heard: 'Hello, world! 28'
^C[INFO] [1666157625.402706029] [rclcpp]: signal_handler(signum=2)
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ 
```
## try a demo
```
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ source /opt/ros/humble/setup.bash
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ ros2 run examples_rclcpp_minimal_publisher publisher_member_function
[INFO] [1666157611.371112594] [minimal_publisher]: Publishing: 'Hello, world! 0'
[INFO] [1666157611.871710499] [minimal_publisher]: Publishing: 'Hello, world! 1'
[INFO] [1666157612.371250088] [minimal_publisher]: Publishing: 'Hello, world! 2'
[INFO] [1666157612.871297227] [minimal_publisher]: Publishing: 'Hello, world! 3'
[INFO] [1666157613.371522167] [minimal_publisher]: Publishing: 'Hello, world! 4'
[INFO] [1666157613.871844896] [minimal_publisher]: Publishing: 'Hello, world! 5'
[INFO] [1666157614.371880821] [minimal_publisher]: Publishing: 'Hello, world! 6'
[INFO] [1666157614.872201094] [minimal_publisher]: Publishing: 'Hello, world! 7'
[INFO] [1666157615.371435881] [minimal_publisher]: Publishing: 'Hello, world! 8'
[INFO] [1666157615.871441313] [minimal_publisher]: Publishing: 'Hello, world! 9'
[INFO] [1666157616.370926662] [minimal_publisher]: Publishing: 'Hello, world! 10'
[INFO] [1666157616.871210890] [minimal_publisher]: Publishing: 'Hello, world! 11'
[INFO] [1666157617.371296671] [minimal_publisher]: Publishing: 'Hello, world! 12'
[INFO] [1666157617.871623149] [minimal_publisher]: Publishing: 'Hello, world! 13'
[INFO] [1666157618.372126518] [minimal_publisher]: Publishing: 'Hello, world! 14'
[INFO] [1666157618.872264892] [minimal_publisher]: Publishing: 'Hello, world! 15'
[INFO] [1666157619.372162448] [minimal_publisher]: Publishing: 'Hello, world! 16'
[INFO] [1666157619.871512694] [minimal_publisher]: Publishing: 'Hello, world! 17'
[INFO] [1666157620.370996057] [minimal_publisher]: Publishing: 'Hello, world! 18'
[INFO] [1666157620.871462294] [minimal_publisher]: Publishing: 'Hello, world! 19'
[INFO] [1666157621.371515362] [minimal_publisher]: Publishing: 'Hello, world! 20'
[INFO] [1666157621.871342175] [minimal_publisher]: Publishing: 'Hello, world! 21'
[INFO] [1666157622.371144069] [minimal_publisher]: Publishing: 'Hello, world! 22'
[INFO] [1666157622.871979067] [minimal_publisher]: Publishing: 'Hello, world! 23'
[INFO] [1666157623.371267761] [minimal_publisher]: Publishing: 'Hello, world! 24'
[INFO] [1666157623.871163881] [minimal_publisher]: Publishing: 'Hello, world! 25'
[INFO] [1666157624.372719669] [minimal_publisher]: Publishing: 'Hello, world! 26'
[INFO] [1666157624.871847484] [minimal_publisher]: Publishing: 'Hello, world! 27'
[INFO] [1666157625.372144794] [minimal_publisher]: Publishing: 'Hello, world! 28'
[INFO] [1666157625.871363298] [minimal_publisher]: Publishing: 'Hello, world! 29'
[INFO] [1666157626.371111537] [minimal_publisher]: Publishing: 'Hello, world! 30'
[INFO] [1666157626.871679305] [minimal_publisher]: Publishing: 'Hello, world! 31'
[INFO] [1666157627.371566723] [minimal_publisher]: Publishing: 'Hello, world! 32'
[INFO] [1666157627.871598705] [minimal_publisher]: Publishing: 'Hello, world! 33'
[INFO] [1666157628.371433682] [minimal_publisher]: Publishing: 'Hello, world! 34'
[INFO] [1666157628.872488578] [minimal_publisher]: Publishing: 'Hello, world! 35'
[INFO] [1666157629.371973314] [minimal_publisher]: Publishing: 'Hello, world! 36'
[INFO] [1666157629.870888122] [minimal_publisher]: Publishing: 'Hello, world! 37'
[INFO] [1666157630.372145951] [minimal_publisher]: Publishing: 'Hello, world! 38'
[INFO] [1666157630.871889609] [minimal_publisher]: Publishing: 'Hello, world! 39'
[INFO] [1666157631.371360854] [minimal_publisher]: Publishing: 'Hello, world! 40'
[INFO] [1666157631.872030503] [minimal_publisher]: Publishing: 'Hello, world! 41'
[INFO] [1666157632.371525641] [minimal_publisher]: Publishing: 'Hello, world! 42'
[INFO] [1666157632.871534418] [minimal_publisher]: Publishing: 'Hello, world! 43'
[INFO] [1666157633.371104469] [minimal_publisher]: Publishing: 'Hello, world! 44'
[INFO] [1666157633.871348657] [minimal_publisher]: Publishing: 'Hello, world! 45'
[INFO] [1666157634.371232464] [minimal_publisher]: Publishing: 'Hello, world! 46'
[INFO] [1666157634.871501780] [minimal_publisher]: Publishing: 'Hello, world! 47'
[INFO] [1666157635.371940587] [minimal_publisher]: Publishing: 'Hello, world! 48'
[INFO] [1666157635.872113217] [minimal_publisher]: Publishing: 'Hello, world! 49'
[INFO] [1666157636.372839542] [minimal_publisher]: Publishing: 'Hello, world! 50'
[INFO] [1666157636.871853980] [minimal_publisher]: Publishing: 'Hello, world! 51'
[INFO] [1666157637.371257244] [minimal_publisher]: Publishing: 'Hello, world! 52'
[INFO] [1666157637.871944843] [minimal_publisher]: Publishing: 'Hello, world! 53'
[INFO] [1666157638.371349710] [minimal_publisher]: Publishing: 'Hello, world! 54'
[INFO] [1666157638.871049576] [minimal_publisher]: Publishing: 'Hello, world! 55'
[INFO] [1666157639.371138345] [minimal_publisher]: Publishing: 'Hello, world! 56'
[INFO] [1666157639.870969210] [minimal_publisher]: Publishing: 'Hello, world! 57'
[INFO] [1666157640.371173227] [minimal_publisher]: Publishing: 'Hello, world! 58'
[INFO] [1666157640.871686742] [minimal_publisher]: Publishing: 'Hello, world! 59'
[INFO] [1666157641.371524839] [minimal_publisher]: Publishing: 'Hello, world! 60'
[INFO] [1666157641.871722992] [minimal_publisher]: Publishing: 'Hello, world! 61'
[INFO] [1666157642.371878215] [minimal_publisher]: Publishing: 'Hello, world! 62'
[INFO] [1666157642.871167292] [minimal_publisher]: Publishing: 'Hello, world! 63'
[INFO] [1666157643.371069121] [minimal_publisher]: Publishing: 'Hello, world! 64'
[INFO] [1666157643.871080299] [minimal_publisher]: Publishing: 'Hello, world! 65'
[INFO] [1666157644.371156413] [minimal_publisher]: Publishing: 'Hello, world! 66'
[INFO] [1666157644.871023933] [minimal_publisher]: Publishing: 'Hello, world! 67'
[INFO] [1666157645.371452539] [minimal_publisher]: Publishing: 'Hello, world! 68'
[INFO] [1666157645.871885349] [minimal_publisher]: Publishing: 'Hello, world! 69'
[INFO] [1666157646.371199945] [minimal_publisher]: Publishing: 'Hello, world! 70'
[INFO] [1666157646.870984199] [minimal_publisher]: Publishing: 'Hello, world! 71'
[INFO] [1666157647.371435886] [minimal_publisher]: Publishing: 'Hello, world! 72'
[INFO] [1666157647.871185284] [minimal_publisher]: Publishing: 'Hello, world! 73'
[INFO] [1666157648.371177110] [minimal_publisher]: Publishing: 'Hello, world! 74'
[INFO] [1666157648.871854597] [minimal_publisher]: Publishing: 'Hello, world! 75'
[INFO] [1666157649.371510518] [minimal_publisher]: Publishing: 'Hello, world! 76'
[INFO] [1666157649.871849284] [minimal_publisher]: Publishing: 'Hello, world! 77'
[INFO] [1666157650.371887618] [minimal_publisher]: Publishing: 'Hello, world! 78'
[INFO] [1666157650.872146664] [minimal_publisher]: Publishing: 'Hello, world! 79'
[INFO] [1666157651.372446555] [minimal_publisher]: Publishing: 'Hello, world! 80'
[INFO] [1666157651.871630323] [minimal_publisher]: Publishing: 'Hello, world! 81'
[INFO] [1666157652.372222036] [minimal_publisher]: Publishing: 'Hello, world! 82'
[INFO] [1666157652.871937176] [minimal_publisher]: Publishing: 'Hello, world! 83'
[INFO] [1666157653.371220683] [minimal_publisher]: Publishing: 'Hello, world! 84'
[INFO] [1666157653.871141916] [minimal_publisher]: Publishing: 'Hello, world! 85'
[INFO] [1666157654.371245694] [minimal_publisher]: Publishing: 'Hello, world! 86'
[INFO] [1666157654.871066695] [minimal_publisher]: Publishing: 'Hello, world! 87'
[INFO] [1666157655.371025806] [minimal_publisher]: Publishing: 'Hello, world! 88'
[INFO] [1666157655.871437232] [minimal_publisher]: Publishing: 'Hello, world! 89'
[INFO] [1666157656.371040925] [minimal_publisher]: Publishing: 'Hello, world! 90'
[INFO] [1666157656.871045026] [minimal_publisher]: Publishing: 'Hello, world! 91'
[INFO] [1666157657.371676517] [minimal_publisher]: Publishing: 'Hello, world! 92'
[INFO] [1666157657.872081514] [minimal_publisher]: Publishing: 'Hello, world! 93'
[INFO] [1666157658.372159591] [minimal_publisher]: Publishing: 'Hello, world! 94'
[INFO] [1666157658.871358875] [minimal_publisher]: Publishing: 'Hello, world! 95'
[INFO] [1666157659.371078453] [minimal_publisher]: Publishing: 'Hello, world! 96'
[INFO] [1666157659.871541323] [minimal_publisher]: Publishing: 'Hello, world! 97'
[INFO] [1666157660.371670431] [minimal_publisher]: Publishing: 'Hello, world! 98'
[INFO] [1666157660.871278872] [minimal_publisher]: Publishing: 'Hello, world! 99'
[INFO] [1666157661.371555303] [minimal_publisher]: Publishing: 'Hello, world! 100'
[INFO] [1666157661.871334031] [minimal_publisher]: Publishing: 'Hello, world! 101'
[INFO] [1666157662.372457007] [minimal_publisher]: Publishing: 'Hello, world! 102'
[INFO] [1666157662.871522120] [minimal_publisher]: Publishing: 'Hello, world! 103'
[INFO] [1666157663.371658583] [minimal_publisher]: Publishing: 'Hello, world! 104'
[INFO] [1666157663.872413110] [minimal_publisher]: Publishing: 'Hello, world! 105'
[INFO] [1666157664.371820340] [minimal_publisher]: Publishing: 'Hello, world! 106'
[INFO] [1666157664.871574714] [minimal_publisher]: Publishing: 'Hello, world! 107'
[INFO] [1666157665.372007896] [minimal_publisher]: Publishing: 'Hello, world! 108'
[INFO] [1666157665.871617209] [minimal_publisher]: Publishing: 'Hello, world! 109'
[INFO] [1666157666.371239570] [minimal_publisher]: Publishing: 'Hello, world! 110'
[INFO] [1666157666.871313272] [minimal_publisher]: Publishing: 'Hello, world! 111'
[INFO] [1666157667.371317097] [minimal_publisher]: Publishing: 'Hello, world! 112'
[INFO] [1666157667.871972198] [minimal_publisher]: Publishing: 'Hello, world! 113'
[INFO] [1666157668.371263890] [minimal_publisher]: Publishing: 'Hello, world! 114'
[INFO] [1666157668.872081011] [minimal_publisher]: Publishing: 'Hello, world! 115'
[INFO] [1666157669.371498123] [minimal_publisher]: Publishing: 'Hello, world! 116'
[INFO] [1666157669.871861393] [minimal_publisher]: Publishing: 'Hello, world! 117'
[INFO] [1666157670.371613807] [minimal_publisher]: Publishing: 'Hello, world! 118'
[INFO] [1666157670.871566020] [minimal_publisher]: Publishing: 'Hello, world! 119'
[INFO] [1666157671.372127941] [minimal_publisher]: Publishing: 'Hello, world! 120'
[INFO] [1666157671.871761079] [minimal_publisher]: Publishing: 'Hello, world! 121'
[INFO] [1666157672.372010714] [minimal_publisher]: Publishing: 'Hello, world! 122'
[INFO] [1666157672.871703389] [minimal_publisher]: Publishing: 'Hello, world! 123'
[INFO] [1666157673.371423477] [minimal_publisher]: Publishing: 'Hello, world! 124'
[INFO] [1666157673.872184025] [minimal_publisher]: Publishing: 'Hello, world! 125'
[INFO] [1666157674.372488848] [minimal_publisher]: Publishing: 'Hello, world! 126'
[INFO] [1666157674.871783927] [minimal_publisher]: Publishing: 'Hello, world! 127'
[INFO] [1666157675.371132341] [minimal_publisher]: Publishing: 'Hello, world! 128'
[INFO] [1666157675.871205477] [minimal_publisher]: Publishing: 'Hello, world! 129'
[INFO] [1666157676.371193285] [minimal_publisher]: Publishing: 'Hello, world! 130'
[INFO] [1666157676.871809417] [minimal_publisher]: Publishing: 'Hello, world! 131'
[INFO] [1666157677.371305281] [minimal_publisher]: Publishing: 'Hello, world! 132'
[INFO] [1666157677.872170226] [minimal_publisher]: Publishing: 'Hello, world! 133'
[INFO] [1666157678.371385578] [minimal_publisher]: Publishing: 'Hello, world! 134'
[INFO] [1666157678.871640007] [minimal_publisher]: Publishing: 'Hello, world! 135'
[INFO] [1666157679.372062410] [minimal_publisher]: Publishing: 'Hello, world! 136'
[INFO] [1666157679.871262145] [minimal_publisher]: Publishing: 'Hello, world! 137'
[INFO] [1666157680.371507405] [minimal_publisher]: Publishing: 'Hello, world! 138'
[INFO] [1666157680.871940348] [minimal_publisher]: Publishing: 'Hello, world! 139'
[INFO] [1666157681.372081001] [minimal_publisher]: Publishing: 'Hello, world! 140'
^C[INFO] [1666157681.581692238] [rclcpp]: signal_handler(signum=2)
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ 
```

# Create a workspace 
## Source  Ros2 evniroment
```
 source /opt/ros/humble/setup.bash

```
## Creating a new directory
```
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws/src
```
## Clone a sample repo
```
git clone https://github.com/ros/ros_tutorials.git -b humble-devel
```
## Resolve the dependencies
```
# cd if you're still in the ``src`` directory with the ``ros_tutorials`` clone
cd ..
rosdep install -i --from-path src --rosdistro humble -y
```
```
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ source /opt/ros/humble/setup.bash
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ mkdir -p ~/ros2_ws/src
cd ~/ros2_ws/src
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws/src$ git clone https://github.com/ros/ros_tutorials.git -b humble-devel
fatal: destination path 'ros_tutorials' already exists and is not an empty directory.
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws/src$ # cd if you're still in the ``src`` directory with the ``ros_tutorials`` clone
cd ..
rosdep install -i --from-path src --rosdistro humble -y
#All required rosdeps installed successfully
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ 

```
# Building a workspace with colcon
```

izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ colcon build
[1.785s] WARNING:colcon.colcon_core.package_selection:Some selected packages are already built in one or more underlay workspaces:
	'examples_rclcpp_minimal_action_client' is in: /opt/ros/humble
	'examples_rclcpp_minimal_client' is in: /opt/ros/humble
	'examples_rclpy_minimal_subscriber' is in: /opt/ros/humble
	'examples_rclpy_minimal_action_server' is in: /opt/ros/humble
	'examples_rclcpp_minimal_composition' is in: /opt/ros/humble
	'examples_rclcpp_minimal_subscriber' is in: /opt/ros/humble
	'examples_rclcpp_minimal_service' is in: /opt/ros/humble
	'turtlesim' is in: /opt/ros/humble
	'action_tutorials_interfaces' is in: /opt/ros/humble
	'examples_rclpy_minimal_publisher' is in: /opt/ros/humble
	'examples_rclcpp_multithreaded_executor' is in: /opt/ros/humble
	'examples_rclpy_minimal_client' is in: /opt/ros/humble
	'examples_rclcpp_minimal_timer' is in: /opt/ros/humble
	'examples_rclcpp_minimal_action_server' is in: /opt/ros/humble
	'examples_rclcpp_minimal_publisher' is in: /opt/ros/humble
	'examples_rclpy_minimal_service' is in: /opt/ros/humble
	'examples_rclpy_executors' is in: /opt/ros/humble
	'examples_rclpy_minimal_action_client' is in: /opt/ros/humble
If a package in a merged underlay workspace is overridden and it installs headers, then all packages in the overlay must sort their include directories by workspace order. Failure to do so may result in build failures or undefined behavior at run time.
If the overridden package is used by another package in any underlay, then the overriding package in the overlay must be API and ABI compatible or undefined behavior at run time may occur.

If you understand the risks and want to override a package anyways, add the following to the command line:
	--allow-overriding action_tutorials_interfaces examples_rclcpp_minimal_action_client examples_rclcpp_minimal_action_server examples_rclcpp_minimal_client examples_rclcpp_minimal_composition examples_rclcpp_minimal_publisher examples_rclcpp_minimal_service examples_rclcpp_minimal_subscriber examples_rclcpp_minimal_timer examples_rclcpp_multithreaded_executor examples_rclpy_executors examples_rclpy_minimal_action_client examples_rclpy_minimal_action_server examples_rclpy_minimal_client examples_rclpy_minimal_publisher examples_rclpy_minimal_service examples_rclpy_minimal_subscriber turtlesim

This may be promoted to an error in a future release of colcon-override-check.
Starting >>> action_tutorials_interfaces
Starting >>> examples_rclcpp_async_client
--- stderr: action_tutorials_interfaces
CMake Error at /opt/ros/humble/share/rosidl_cmake/cmake/rosidl_generate_interfaces.cmake:93 (message):
  rosidl_generate_interfaces() the passed file 'action/Fibonacci.action'
  doesn't exist relative to the CMAKE_CURRENT_SOURCE_DIR
  '/home/izzatullokh/ros2_ws/src/ros2_ws/src/action_tutorials_interfaces'
Call Stack (most recent call first):
  CMakeLists.txt:28 (rosidl_generate_interfaces)


---
Failed   <<< action_tutorials_interfaces [1.42s, exited with code 1]
Aborted  <<< examples_rclcpp_async_client [3.28s]                            

Summary: 0 packages finished [4.26s]
  1 package failed: action_tutorials_interfaces
  1 package aborted: examples_rclcpp_async_client
  1 package had stderr output: action_tutorials_interfaces
  25 packages not processed
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ 

```
