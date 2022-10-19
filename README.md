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
