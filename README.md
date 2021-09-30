# Create-an-ai-model-from-the-technology-of-your-choice-to-detect-and-label-defects-in-the-casting-pro

YOLOV4 model trainned



video_link ==:  https://youtu.be/1YkyD0WTcws



Requirements for Windows
CMake >= 3.18: https://cmake.org/download/
Powershell (already installed on windows): https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershel
CUDA >= 10.2: https://developer.nvidia.com/cuda-toolkit-archive (on Linux do Post-installation Actions)
OpenCV >= 2.4: use your preferred package manager (brew, apt), build from source using vcpkg or download from OpenCV official site (on Windows set system variable OpenCV_DIR = C:\opencv\build - where are the include and x64 folders image)
cuDNN >= 8.0.2 https://developer.nvidia.com/rdp/cudnn-archive (on Linux copy cudnn.h,libcudnn.so... as described here https://docs.nvidia.com/deeplearning/sdk/cudnn-install/index.html#installlinux-tar , on Windows copy cudnn.h,cudnn64_7.dll, cudnn64_7.lib as described here https://docs.nvidia.com/deeplearning/sdk/cudnn-install/index.html#installwindows )
GPU with CC >= 3.0: https://en.wikipedia.org/wiki/CUDA#GPUs_supported



STEP:1 --   DOWNLOAD folder from google drive (inside trainned model)(due to large file & size ,it  not uploaded on Github  )

link:----   https://drive.google.com/drive/folders/1aIdj4OziHSQaJqQcowAIKtSYhifgvflK?usp=sharing





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




reference:---- https://github.com/AlexeyAB/darknet.git
