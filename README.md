# ROS AWS Utils Common Library


## Overview
This is the common library for all of AWS RoboMaker packages.

### License
The source code is released under an [Apache 2.0].

**Author**: AWS RoboMaker<br/>
**Affiliation**: [Amazon Web Services (AWS)]<br/>
**Maintainer**: AWS RoboMaker, ros-contributions@amazon.com

### Supported ROS Distributions
- Melodic

### Build status
* GitHub Action Status
     * master: [![Build & Test](https://github.com/aws-robotics/utils-common/workflows/Build%20&%20Test/badge.svg?branch=master&event=schedule)](https://github.com/aws-robotics/utils-common/actions?query=workflow%3A"Build+%26+Test"+event%3Aschedule)
     * release-latest: [![Build & Test release-latest](https://github.com/aws-robotics/utils-common/workflows/Build%20&%20Test%20release-latest/badge.svg?branch=master&event=schedule)](https://github.com/aws-robotics/utils-common/actions?query=workflow%3A"Build+%26+Test+release-latest"+event%3Aschedule)
* ROS build farm:
    * ROS Kinetic @ u16.04 Xenial [![Build Status](http://build.ros.org/job/Kbin_uX64__aws_common__ubuntu_xenial_amd64__binary/badge/icon)](http://build.ros.org/job/Kbin_uX64__aws_common__ubuntu_xenial_amd64__binary)
    * ROS Melodic @ u18.04 Bionic [![Build Status](http://build.ros.org/job/Mbin_uB64__aws_common__ubuntu_bionic_amd64__binary/badge/icon)](http://build.ros.org/job/Mbin_uB64__aws_common__ubuntu_bionic_amd64__binary)
    * ROS Dashing @ u18.04 Bionic [![Build Status](http://build.ros2.org/job/Dbin_uB64__aws_common__ubuntu_bionic_amd64__binary/badge/icon)](http://build.ros2.org/job/Dbin_uB64__aws_common__ubuntu_bionic_amd64__binary)

## Installation

### Binaries
On Ubuntu you can install the latest released version of this package using the following command

        sudo apt-get update
        sudo apt-get install -y ros-$ROS_DISTRO-aws-common

### Building from Source

To build from source you'll need to create a new workspace, clone and checkout the latest release branch of this repository, install all the dependencies, and compile. If you need the latest development features you can clone from the `master` branch instead of the latest release branch. While we guarantee the release branches are stable, __the `master` should be considered to have an unstable build__ due to ongoing development. 

- Install build tool: please refer to `colcon` [installation guide](https://colcon.readthedocs.io/en/released/user/installation.html)

- Create a ROS workspace and a source directory

        mkdir -p ~/ros-workspace/src

- Clone the package into the source directory. 

        cd ~/ros-workspace/src
        git clone https://github.com/aws-robotics/utils-common.git -b release-latest

- Install dependencies

        cd ~/ros-workspace 
        sudo apt-get update && rosdep update
        rosdep install --from-paths src --ignore-src -r -y
        
_Note: If building the master branch instead of a release branch you may need to also checkout and build the master branches of the packages this package depends on._

- Build the packages

        cd ~/ros-workspace && colcon build

- Configure ROS library path

        source ~/ros-workspace/install/local_setup.bash


[Amazon Web Services (AWS)]: https://aws.amazon.com/
[Apache 2.0]: https://aws.amazon.com/apache-2-0/
