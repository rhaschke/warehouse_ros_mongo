# Warehouse ROS Mongo Interface

Code for persisting ROS message data using MongoDB.  Contains C++ and Python libraries to serialize ROS data to MongoDB, as well as some handy scripts to record data from the command line.  Based on code split out of warehouse_ros.

## GitHub Actions - Continuous Integration

[![Format](https://github.com/ros-planning/warehouse_ros_mongo/actions/workflows/format.yml/badge.svg?branch=noetic-devel)](https://github.com/ros-planning/warehouse_ros_mongo/actions/workflows/format.yml?branch=noetic-devel) [![BuildAndTest](https://github.com/ros-planning/warehouse_ros_mongo/actions/workflows/industrial_ci_action.yml/badge.svg?branch=noetic-devel)](https://github.com/ros-planning/warehouse_ros_mongo/actions/workflows/industrial_ci_action.yml?branch=noetic-devel)

## Building from source

### ROS Jade  / Kinetic

In order to build from source you'll need to install the [mongo c++ drivers](https://github.com/mongodb/mongo-cxx-driver/wiki/Download-and-Compile-the-Legacy-Driver)

First get the driver:
```
git clone -b 26compat https://github.com/mongodb/mongo-cxx-driver.git
```

Then compile using scons:
```
sudo apt-get install scons
cd mongo-cxx-driver
sudo scons --prefix=/usr/local/ --full --use-system-boost --disable-warnings-as-errors
```

You should now be able to compile the packages using catkin.
