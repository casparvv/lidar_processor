## LiDAR Processor
Basic ROS package for point cloud processing of LiDAR data

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
4. Run package:
```
rosrun lidar_processor lidar_processor
```

### To do:
- Test
- Adjust filtering of PCL to get constant number of points:
- https://pcl.readthedocs.io/projects/tutorials/en/master/remove_outliers.html#remove-outliers
- https://pointclouds.org/documentation/classpcl_1_1_conditional_removal.html
- https://pcl.readthedocs.io/projects/tutorials/en/master/statistical_outlier.html#statistical-outlier-removal

#### References
- https://wiki.ros.org/pcl/Tutorials
- https://pointclouds.org/documentation/
- https://pcl.readthedocs.io/en/latest/voxel_grid.html

