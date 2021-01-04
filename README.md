# endToEnd_stereoLocalization

### 1. TITLE: 

Screw Drivers database for 3D stereo object localization

### 2. CONTACT: 

[Joris GUERIN](https://jorisguerin.github.io/)  
Laboratoire d'Ingénierie des Systèmes Physiques Et Numériques, Arts et Métiers ParisTech, Lille, France  
Ecole Nationale supérieure des Arts et Métiers  
8 Boulevard Louis XIV  
59800 LILLE  
FRANCE  
email: jorisguerin.research@gmail.com

### 3. RELEVANT INFORMATION:

This folder contains a labelled dataset for 3D object localization. Each example is composed of two 300x300 images (from two fixed cameras) and the target is a vector with 6 entries representing the XYZ coordinates of two points on the screw driver handle. The two points are the uppest and lowest point of the handle on the screw driver axis.

This dataset was generated using an industrial robot to get knowledge of the exact position of the object. The XYZ coordinates are expressed in the robot frame, hence the 3D localization model needs to handle the change of frame.

A computer vision algorithm was implemented to remove the robot from some of the images. For other cases, we hide the robot physically with a t-shirt wrapped around the effector. The information relative to the situation, as well as the screw driver present on the two images can be found in the 'info.txt' file.
More information can be found on the paper (see citation)

### 5. NUMBER OF INSTANCES:

5008 examples (10016 images (300x300))

### 6. INPUT FEATURES:

Each example is composed of two 300x300 images from two cameras.

These images are meant to be the inputs of a regression model for 3D object localization using stereo vision. For each example, both images were taken simultaneously. Focal lengthes, positions and orientations of both cameras are fixed among all the examples in the dataset.

Corresponding images have the same file name in the folders "cam1" and "cam2".

### 7. TARGETS:

The "targets.txt" file contains the position labels of the dataset.

The first row corresponds to the couple of images "0.jpg", the second row to "1.jpg", and so on...

Each target is composed of 6 entries separated by semicolumns: "x_pt1;y_pt1;z_pt1;x_pt2;y_pt2;z_pt2"

### 8. ADDITIONAL INFORMATION:

Additional information about the data can be found in the "info.txt" file.

Each line of this file contains the screw driver model (1, 2, 3 or 4) and the presence of the robot (a, b, c) separated by a semicolumn.

Presence of the robot:
* a : robot is on the image
* b : end-effector hidden with a t-shirt
* c : robot removed computationally

### 9. CITATION:

If you find this dataset useful in your research, please consider citing:

		@inproceedings{guerin2018automatic,
		title={Automatic Construction of Real-World Datasets for 3D Object Localization using Two Cameras},
		author={Gu{\'e}rin, Joris and Gibaru, Olivier and Nyiri, Eric and Thiery, St{\'e}phane and Palos, Jorge},
		booktitle={IECON 2018-44th Annual Conference of the IEEE Industrial Electronics Society},
		pages={3655--3658},
		year={2018},
		organization={IEEE}
		}


### 10. MISSING ATTRIBUTE VALUES: None
