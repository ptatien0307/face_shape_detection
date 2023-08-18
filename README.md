
# Face shape detection

A project make use of deep learning and facial landmark to detect human's face shape
There's will be 5 type of shapes: square, heart, oval, long, round

# Dataset
Dataset is taken from https://www.katebloom.co.uk/blog/entry/determine-your-face-shape

# Model
* VGG16
* ResNet50
* SVM
* Random Forest
* KNN
   
# Method
* **Landmark**: using **mediapipe** to detect landmark
  * Find face
  * Detect landmark
  * Calculate ratio based on features
    * D1 - Face length
    * D2 - Forehead width
    * D3 - Cheekbone width
    *	D4 - Jaw width
    * D5 - Jawline length
    * D6 - Chin width 1
    * D7 - Chin width 2
    * A1, A2, A3
<p align="center">
<img src="https://github.com/ptatien0307/face_shape_detection/assets/79583501/00b05872-a809-4c90-be7a-a7b7e5bb407c.png" alt="drawing" width="75%" height="75%"/>
</p>

<p align="center">
<img src="https://github.com/ptatien0307/face_shape_detection/assets/79583501/cec0a0dd-570e-431a-960f-bf3a17e84692.png" alt="drawing" width="75%" height="75%"/>
</p>
 
  * Calculate Ratio: These ratios will be feed into model to dectect face shape
    * R1 = D2 / D3
    *	R2 = D3 / D1
    *	R3 = D2 / D1
    *	R4 = D2 / D4
    *	R5 = D6 / D4
    *	R6 = D5 / D6
    *	R7 =  D6 / D3
    *	R8 = D5 / D2
    *	R9 = D5 / D4
    *	R10 = D7 / D6

* **Machine learning model**
  * Step 1: Find face
  * Step 2: Detect face shape
<p align="center">
<img src="https://github.com/ptatien0307/face_shape_detection/assets/79583501/ed234aad-8cd0-4739-a9b1-019260912041.png" alt="drawing" width="75%" height="75%"/>
</p>
