# SocialDistancingDetector

This code allows you to detect people in a video file and for every person in the video, shows the level of risk.
What it basically does is quite simple, using pretrained models from yolov3, it detects a person and between every person it finds the euclidean distance.
The distance found thus divides every person into high risk/low risk groups.

Using the distance, we use rectangles to detect every person.
Red - High risk
Yellow - Low risk
Green - Safe

Also for the objects in risk we have used straight lines to connect their centers. 
Yellow and Red lines are used to connect the objects close to each other. The colour is based on the list mentioned above.


For the code to work, the input video must named as 'video.mp4'. I am not sure yet about the other video types. This project not only runs in real time but also after its execution, creates an output video .

The yolov3.cfg, yolov3.weights and coco.names files are obtained by cloning the darknet repository.
