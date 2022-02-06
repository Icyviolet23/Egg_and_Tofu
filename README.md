# Egg and Tofu (https://www.youtube.com/watch?v=9WPAkc6xg0I)
Eggs and tofus are raining from the sky! These food are generated according to the beats of the background music, with a rare tofu appearing very occasionally alongside eggs. To avoid being hit by the falling food, you would have to slice these falling food on the screen before they reach the ground. Use a flashlight and wave it in front of your webcam to slice the food. There will be a line appearing on the screen indicating the slicing path of your flashlight. Try to get as many of the food as possible before the music ends. Good luck! :) 

## Modules to be installed
* PyGame
* OpenCV
* PyWavelets
* Scipy
* Numpy
* Matplotlib
* Argparse

## Description
### Beat Detection
* The BPM Detector is used to process the audio files and outputs the bpm of the audio.
* Before the start of the game, the user selects a song out of the options available: Nocturne op.9 No.2, Moonlight Sonata and Stereo Madness.
* The BPM of the song choice will determine the rate at which the falling foods are generated in the game.

### OpenCV
* OpenCV was used to capture a video stream from the user's webcam. Each frame in the video feed is filtered to grayscale and Gaussian blur was applied, before the brightest area in the frame is found. This function outputs the x,y coordinates of the brightest area.

### User Interface
* Based on the x,y coordinates of the brightest area, a queue of coordinates is stored and being constantly updated when the user moves the flashlight around.
* The raw coordinates are being processed to find the statistical mean of every 5 points, using this processed data to generate a line which is the slicing path.
* The foods are being represented by bounding boxes consisting of 4 line segments. When the slicing path of the user intersects with any of the line segments bounding the foods, the food would be considered as sliced by the user.

## Instructions for running

Play this game in a room with dim light conditions or a dark background. 

A phone with flashlight is required for the user to interact with the game.

A laptop with a webcam is also required.

**To start the program, run main.py**

**Follow the instructions in the console to select a song before starting the game.**

