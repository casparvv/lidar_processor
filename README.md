## LiDAR/LaserScan Processor
Basic ROS package for processing of LiDAR data consisting of two nodes, (1) for LaserScan data and (2) for PointCloud data. 

1. LiDAR LaserScan data
- Subscribes to `/scan` and calculates 3D points from the distances and angles.
- Publishes output as PointCloud to `/scan_pointcloud`.

2. LiDAR PointCloud data
- Subscribes to `/lidar/pointcloud` and runs a simple callback function that downsamples the data with a VoxelGrid filter.
- Publishes output to `/point_cloud_filtered`.

### Usage
1. Clone into your ROS workspace `src` directory
```
git clone git@github.com:casparvv/lidar_processor.git
```
2. Build the package from workspace
```
catkin_make
```
3. Source workspace
```
source devel/setup.bash
```
4. Run package

(1) LiDAR LaserScan data
```
rosrun lidar_processor laser_scan_processor.py
```
(2) LiDAR PointCloud data
```
rosrun lidar_processor lidar_processor
```

#### References
- https://wiki.ros.org/pcl/Tutorials
- https://pointclouds.org/documentation/
- https://pcl.readthedocs.io/en/latest/voxel_grid.html
- https://docs.ros.org/en/noetic/api/sensor_msgs/html/msg/LaserScan.html

