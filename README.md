STEP1
下載final_project_1100313.f3d、
final_project_1100313_description.zip
fp1100313.zip
robot_gazebo.zip

下載完成之後，將它們放置到catkin_ws/src底下

STEP2
在終端機執行roscore

STEP3
在終端機執行rviz

STEP4
在終端機執行roslaunch robot_gazebo start_all.launch  (叫出機器人、gazebo環境和啟動SLAM檔)

STEP5
在終端機執行rosrun tf static_transform_publisher x y z yaw pitch roll base_link lidar_1 100

STEP6
在rviz裡
在左下角點選Add，在By display type列表新增RobotModel，如此可在rviz呼叫出機器人
在左下角點選Add，在By display type列表新增Map，如此可看到繪製的地圖
在左下角點選Add，在By display topic列表新增LaserScan

在Global Options底下的Fixed Frame，選擇lidar_1
在Map底下的Topic，選擇/map
在LaserScan底下的Size，調成0.05

STEP7
最後執行rosrun fp1100313 fp_control.py，開始進行機器人智能自動避障，並繪出雷達所偵測到的地圖資料
