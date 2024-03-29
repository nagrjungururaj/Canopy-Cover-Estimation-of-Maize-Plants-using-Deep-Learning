# Canopy-Cover-Estimation-of-Maize-Plants-using-Deep-Learning

# Copyright : 

(Very Important!)
The image data is solely owned and distributed by Digite Inc. and any usage could lead to severe voilations of company's copyright. For obtaining and usage of the data please contact Digite Inc. (https://www.digite.com/)

# Goal : 
The overall goal of the problem is to identify the Canopy Cover Percentage from a given picture / image using deep learning. Further, the problem has intermediate goals as below:  
⦁	From a given image, the designed algorithm is able to differentiate a maize plant from a weed plant  
⦁	Finally, the designed algorithm identifies different stages of a maize from 29JUL19 TO 3AUG19

# Dataset :
⦁	The given dataset consists of 46 images captured using a smart phone in a field containing maize plants along with the weed plant near Bengaluru India.

# Requirements (Note without these code wont run ! ) :

Anaconda, pillow, lxml, Cython, contextlib2, jupyter, matplotlib, pandas, opencv-python

# Download models.zip from here : https://www.dropbox.com/s/w65vb29iki0ylbx/models.zip?dl=0

# Testing on your images
1. Download models.zip and extract models folder.
2. Capture images from a maize field using a smartphone or drone
3. Use labelImg tool to label your images. Tool can be found here : https://github.com/tzutalin/labelImg
4. Place the images in 'images' folder under 'models\research\object_detection'
5. Generate the labels using the command: python xml_to_csv
6. The train and test labels will be in 'images' folder
7. Trained model is already present in 'training' folder
8. Place the images you want to test from your set in 'test_img' folder

# Setup : 
1. Go to models\research\object_detection
2. Run this command corresponding to local path of your environment (Change the paths accordingly)
for example : set PYTHONPATH=C:\Desktop\models;C:\Desktop\models\research;C:\Desktop\models\research\slim (wont run if not executed)

# Run Sequence :
1. Copy all .ipynb to 'models\research\object_detection' folder before doing anything
2. Run the .ipynb files in the following sequence 

   object_detection_maize.ipynb --> calculate_iou.ipynb --> generate_bbox_crops.ipynb --> calculate_canopy_cover.ipynb -->           visualize_canopy_growth.ipynb

# Results : 
The algorithm predicts a rise in the canopy cover through the progression of dates staring from 20 JUL 19 to 3 Aug 19 which is in sync with the theoritical assumption. The algorithm achieves the following root mean square errors for corresponding fields as below, 

RMSE F1 : 0.36239708194589165  
RMSE F3 : 0.14613046722087242  
RMSE F7 : 0.9559942436130704  

Note that the RMSE for F7 is quite large due to the rapid growth and overlap of bounding boxes predicted from the algorithm for the end of a season of peak period.
