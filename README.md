# doggobot_perception

This is a repo that contains 2 launch files to start the perception subsystem in the doggobot.

Please make sure the following repos are cloned into the PC.
1) object_identification_with_keras
2) apriltag_location_to_map
3) image_masking_with_pointclouds_and_colour
4) take_and_upload_photos

Please make sure the following repos are cloned into the doggobot.
1) pcl_ros
2) apriltag_ros
3) object_segmentation_with_pointclouds
4) object_segmentation_with_colour
5) image_masking_with_with_pointclouds_and_colour
6) table_identification_with_apriltags

To run, on the PC, roslaunch the following.
```
roslaunch perception_PC.launch
```

Next, on the doggobot, roslaunch the following. (This should already be inside doggobotics_ros)
```
roslaunch doggobot_bringup perception_doggo.launch
```
