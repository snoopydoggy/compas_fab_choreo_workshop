# Using Docker

This instruction is adapted from the [robotic_assembly_workshop](https://github.com/gramaziokohler/robotic_assembly_workshop/edit/master/docker-help.md).

Docker is a tool that runs and manages **containers**. A container is similar to a very lightweight virtual machine.

For this workshop, we start groups of containers all at once using a command called **docker-compose**. This allows us to run multiple ROS nodes in one go.

This repository mainly uses two groups of containers, each one provides an entire ROS system with different settings:

* **ROS Basic**: a minimal ROS system containing just a master node and a few other nodes required to access it from Windows. [Configuration file](docker/ros-systems/ros-basic/docker-compose.yml).
* **ROS UR5 - Planning**: a ROS system configured with MoveIt! motion planning for a UR5 robot. [Configuration file](docker/ros-systems/ros-ur5/docker-compose.yml).

## How to start docker containers

### From the command prompt

Open your Anaconda prompt (or the command prompt), go to the folder where the `docker-compose.yml` file resides, and run:

    docker-compose up -d

Once you're done with the system, you can remove all containers with:

    docker-compose down

### From Visual Studio Code

If you have the `Docker` extension installed, you can right-click any `docker-compose.yml` file and select `Compose Up` and `Compose Down` to turn the systems on and off.
