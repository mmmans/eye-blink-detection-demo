# eye-blink-detection-demo

 A very simple demo code for eye blink detection with dlib libray with python, Note this project is basically dependent on the library dlib. The methods used in the demo code is introduced in [Paper](http://vision.fe.uni-lj.si/cvww2016/proceedings/papers/05.pdf?spm=a2c4e.11153940.blogcont336184.6.28a771e8bHtjbJ&file=05.pdf). This code is based on the blog[Eye blink detection with OpenCV, Python, and dlib](https://www.pyimagesearch.com/2017/04/24/eye-blink-detection-opencv-python-dlib/). Here is the Chinese translation[OpenCV/Python/dlib眨眼检测](https://yq.aliyun.com/articles/336184). 

## Environment
* win10
* python 3.5.4
* opencv 3.3.1
* imutils 0.4.6
* dlib 18.18
* Anaconda3

## install packages
```
conda intall dlib
conda install opencv3
pip install imutils
```

## sample 
open the terminal 
```
python detect_blinks.py
```
The default args open the camera and detect the eye blink in the video
![sample](https://github.com/mans-men/eye-blink-detection-demo/blob/master/sample.png)

```
python detect_blinks.py -h
optional arguments:
  -h, --help            show this help message and exit
  -p SHAPE_PREDICTOR, --shape-predictor SHAPE_PREDICTOR
                        path to facial landmark predictor
  -v VIDEO, --video VIDEO
                        path to input video file
  -t THRESHOLD, --threshold THRESHOLD
                        threshold to determine closed eyes
  -f FRAMES, --frames FRAMES
                        the number of consecutive frames the eye must be below
                        the threshold
```
You can see more information about the args, parse a larger **threshold** means an eye can be more easily considered as closed, vice versa.parse a larger **frames** means only if the closed eyes last for more frames, can it be considered as a closed eye.You can aslo parse a video file by parsing **video** args. the **shape-predictor** args indicate the trained model path which is provided in the demo


