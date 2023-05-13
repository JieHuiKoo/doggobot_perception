# doggobot_perception

This is a repo that contains 2 launch files to start the perception subsystem in the doggobot.

Please make sure the following repos are cloned into the PC.
1) object_identification_with_keras - For object identification</br>
https://github.com/JieHuiKoo/object_identification_with_keras.git
2) apriltag_location_to_map - Saving poses of Apriltags while robot is exploring</br>
https://github.com/JieHuiKoo/apriltag_location_to_map.git
3) image_masking_with_pointclouds_and_colour - The boundingbox intersecting algorithm. GetPickupCentroid service is hosted on PC.</br>
https://github.com/JieHuiKoo/image_masking_with_pointclouds_and_colour.git
4) take_and_upload_photos - For saving and uploading photos to the database</br>
https://github.com/JieHuiKoo/take_and_upload_photos.git
5) doggobot_picture_vault - Website and Database Server</br>
https://github.com/JieHuiKoo/doggobot_picture_vault.git

Please make sure the following repos are cloned into the doggobot.
1) pcl_ros - For converting Pointcloud to RGB image (Part of bounding box intersecting algorithm)</br>
http://wiki.ros.org/pcl_ros</br>
Should be preinstalled together with ROS Melodic</br>
2) apriltag_ros - For identification of apriltags (Dependency of apriltag_location_to_map)</br>
https://github.com/JieHuiKoo/apriltag_ros.git
3) object_segmentation_with_pointclouds - For object localisation using pointclouds</br>
https://github.com/JieHuiKoo/object_segmentation_with_pointclouds.git
4) object_segmentation_with_colour - For object localisation and identification using RGB</br>
https://github.com/JieHuiKoo/object_segmentation_with_colour.git
5) image_masking_with_with_pointclouds_and_colour - The boundingbox intersecting algorithm</br>
https://github.com/JieHuiKoo/image_masking_with_pointclouds_and_colour.git
6) table_identification_with_apriltags - For alignment to the table using PID (Fine tuning needed, disabled as of May 14 2023)</br>
https://github.com/JieHuiKoo/table_identification_with_apriltags.git

To run:

First, on the PC, roslaunch the following.
```
roslaunch perception_PC.launch
```

Next, on the doggobot, roslaunch the following. (This should already be inside doggobotics_ros)
```
roslaunch doggobot_bringup perception_doggo.launch
```
