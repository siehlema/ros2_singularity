# ros2_singularity

This repository follows the steps of the [ROS2 installation of Dashing from source](https://index.ros.org/doc/ros2/Installation/Dashing/Linux-Development-Setup/) in a Singularity definition file and adds some functionality. Singularity containers can for instance be used from SLURM workload managers on computer clusters.

It is supposed to help new Singularity/ROS2 developers to start their projects.

## How to
* meet prerequisites for demo:
  * Linux environment (tested on Ubuntu 18.04)
  * install Singularity ([Guide](https://sylabs.io/guides/3.0/user-guide/installation.html))
  * run all containers on one host
* clone repo
* build singularity container: `sudo singularity build ros2_container.simg Singularity`
* afterwards try the demo apps:
  * `sudo singularity run --app example_talker ros2_container.simg`
  * `sudo singularity run --app example_listener ros2_container.simg`
* create your own apps on the Singularity container or copy them onto the container before building
