# Real-Time Object Detection with TensorFlow

## Overview
This repository contains the code and documentation for my Bachelor's thesis on real-time object detection using deep learning and TensorFlow. The project utilizes the "SSD MobileNet V2 FPNLite 320x320" pre-trained model provided by TensorFlow. I trained and tested the model using custom data created using LabelImg by Tzutalin GitHub user.

## Introduction
Real-time object detection is a crucial task in computer vision, with applications ranging from surveillance to autonomous vehicles. This project explores the implementation of real-time object detection using deep learning techniques, specifically leveraging the SSD MobileNet V2 FPNLite architecture trained on the TensorFlow platform. Custom data for training and testing was prepared using LabelImg by Tzutalin GitHub user.

## Installation
To set up the project, follow these steps:
1. Clone the repository: https://github.com/pars4sh/TensorFlowObjectDetection <br/><br/>
2. Create a new virtual environment
<pre>python -m venv [your-environment-name]</pre> <br/><br/>
3. Activate your virtual environment
<pre>
source tfod/bin/activate # Linux
.\tfod\Scripts\activate # Windows 
</pre> <br/><br/>
4. Install dependencies and add virtual environment to the Python Kernel
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=[your-environment-name]
</pre> <br/><br/>
5. Collect images using the Notebook 1. Image Collection.ipynb - ensure you change the kernel to the virtual environment <br/><br/>
6. Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. <br/>
\TensorFlowObjectDetection\Tensorflow\workspace\images\train <br/>
\TensorFlowObjectDetection\Tensorflow\workspace\images\test <br/><br/>
7. Begin training process by opening 2. Training and Detection.ipynb, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model. <br/><br/>
8. During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK. 
If not, resolve installation errors by referring to the Error Guide.md in this folder. <br/><br/>
9. Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics. <br/><br/>
10. You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g.
<pre>cd Tensorflow/workspace/models/my_ssd_mobnet/eval</pre>
and open Tensorboard with the following command
<pre>tensorboard --logdir=.</pre>
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
