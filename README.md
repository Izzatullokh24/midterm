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

```


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


izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ . install/setup.bash



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

# Creating a package
```
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ ros2 pkg create --build-type ament_python py_pubsub
going to create a new package
package name: py_pubsub
destination directory: /home/izzatullokh/ros2_ws
package format: 3
version: 0.0.0
description: TODO: Package description
maintainer: ['izzatullokh <izzatullokh@todo.todo>']
licenses: ['TODO: License declaration']
build type: ament_python
dependencies: []
creating folder ./py_pubsub
creating ./py_pubsub/package.xml
creating source folder
creating folder ./py_pubsub/py_pubsub
creating ./py_pubsub/setup.py
creating ./py_pubsub/setup.cfg
creating folder ./py_pubsub/resource
creating ./py_pubsub/resource/py_pubsub
creating ./py_pubsub/py_pubsub/__init__.py
creating folder ./py_pubsub/test
creating ./py_pubsub/test/test_copyright.py
creating ./py_pubsub/test/test_flake8.py
creating ./py_pubsub/test/test_pep257.py

[WARNING]: Unknown license 'TODO: License declaration'.  This has been set in the package.xml, but no LICENSE file has been created.
It is recommended to use one of the ament license identitifers:
Apache-2.0
BSL-1.0
BSD-2.0
BSD-2-Clause
BSD-3-Clause
GPL-3.0-only
LGPL-3.0-only
MIT
MIT-0

```
## Write a publisher node 
```
izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$ wget https://raw.githubusercontent.com/ros2/examples/humble/rclpy/topics/minimal_publisher/examples_rclpy_minimal_publisher/publisher_member_function.py
--2022-10-19 15:03:21--  https://raw.githubusercontent.com/ros2/examples/humble/rclpy/topics/minimal_publisher/examples_rclpy_minimal_publisher/publisher_member_function.py
Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 185.199.110.133, 185.199.111.133, 185.199.108.133, ...
Connecting to raw.githubusercontent.com (raw.githubusercontent.com)|185.199.110.133|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1576 (1.5K) [text/plain]
Saving to: ‘publisher_member_function.py’

publisher_member_fu 100%[===================>]   1.54K  --.-KB/s    in 0.001s  

2022-10-19 15:03:21 (2.51 MB/s) - ‘publisher_member_function.py’ saved [1576/1576]

izzatullokh@izzatullokh-virtual-machine:~/ros2_ws$

```
## I opened my code editor visual studio and wrote following code:
```
# Copyright 2016 Open Source Robotics Foundation, Inc.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

import rclpy
from rclpy.node import Node

from std_msgs.msg import String


class MinimalPublisher(Node):

    def __init__(self):
        super().__init__('minimal_publisher')
        self.publisher_ = self.create_publisher(String, 'topic', 10)
        timer_period = 0.5  # seconds
        self.timer = self.create_timer(timer_period, self.timer_callback)
        self.i = 0

    def timer_callback(self):
        msg = String()
        msg.data = 'Hello World: %d' % self.i
        self.publisher_.publish(msg)
        self.get_logger().info('Publishing: "%s"' % msg.data)
        self.i += 1


def main(args=None):
    rclpy.init(args=args)

    minimal_publisher = MinimalPublisher()

    rclpy.spin(minimal_publisher)

    # Destroy the node explicitly
    # (optional - otherwise it will be done automatically
    # when the garbage collector destroys the node object)
    minimal_publisher.destroy_node()
    rclpy.shutdown()


if __name__ == '__main__':
    main()
```

