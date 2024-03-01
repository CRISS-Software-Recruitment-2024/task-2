# task-2
In this task we will explore ros services and how clients and servers interact with each other 

IMPORTANT NOTE: The tutorial at https://github.com/CRISS-Robotics/learn-ros is a pre-requisite for this task. If you haven't completed the tutorial, do that first.

Task 2: Services in ROS
Introduction : Understanding services https://www.youtube.com/watch?v=qhnlmrGQVvM&t=429s

STEP 1: Read http://wiki.ros.org/rospy/Overview/Services
        Watch https://www.youtube.com/watch?v=zQL0pEVZDKQ
 
STEP 2: How will we implement services? Remember how we made our mobile manipulator move by publishing on the ```/robot_base_velocity_controller/cmd_vel``` topic. Now lets say I give you an integer called sec_int and then tell you to make the robot move in x direction with velocity=1m/s for the duration of sec_int. (say sec_int =5 , then the rover should move in the x direction for 5 seconds). Services make this task very easy and intuative. Okay you this is what you will do.

STEP 3: Create a server called velocity_control_server.py in the src folder. Create velocity.srv file in the srv folder ( i have attached a screenshot of how the file structure should look like also it contains how the srv file should look like).

![WhatsApp Image 2024-02-29 at 23 42 43](https://github.com/CRISS-Software-Recruitment-2024/task-2/assets/83595034/6a9f2db2-3665-4ae8-822a-d94ac8f76bec)

STEP 4: Add code in velocity_control_server.py . Follow this video https://www.youtube.com/watch?v=zQL0pEVZDKQ. It will help you guide through the task . Also you should be make the needed changes to the package.xml file and the CMakeLists.txt . These changes are in the video . Change these files carefully. http://wiki.ros.org/ROS/Tutorials/CreatingMsgAndSrv this link gives an overview for the same.

STEP 5: run the command ```rosservice call /velocity_change_service "sec_int: 9"```
        Note: Here the service name is ```/velocity_change_service``` which you define in the velocity_control_server.py file

STEP 6: You need to upload the ```velocity_control_server.py``` here as your submission.
