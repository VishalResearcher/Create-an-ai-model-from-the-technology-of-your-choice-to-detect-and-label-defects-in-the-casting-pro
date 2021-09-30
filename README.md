# Create-an-ai-model-from-the-technology-of-your-choice-to-detect-and-label-defects-in-the-casting-pro
YOLOV4 OBJECT DETECTION


there are mainly two categories:-
1) Defective (COLOR PINK)

2) NoDefective (COLOR GREEN) 



IMAGE ANNOTATION 

software :  https://cvat.org/

then 

open cmd
go to x64 folder then type command
for trainned image
~/darknet.exe detector train data/obj3.data cfg/yolov4-obj3.cfg yolov4.weights

for camrera
~/darknet.exe detector demo data/obj3.data cfg/yolov4-obj3.cfg backup/yolov4-obj3_last.weights -c 0

for camera & threshold
~/darknet.exe detector demo data/obj3.data cfg/yolov4-obj3.cfg backup/yolov4-obj3_last.weights -c 0 -thresh value   #value float 0.5,0.6,0.7 


for video 
~/darknet.exe detector demo data/obj3.data cfg/yolov4-obj3.cfg backup/yolov4-obj3_last.weights video.mp4


for image
~/darknet.exe detector test data/obj3.data cfg/yolov4-obj3.cfg backup/yolov4-obj3_last.weights

