# bmicp (stomatal pore quantifier)

A three step image analysis program for quantification of stomatal aperture from bright field images.

1. Identifying the coordinate of the stomata by HOG + SVM.
2. Classifying the status (open, partially open, closed, false positive) by CNN.
3. Pore quantification responsive to the object status.

<img src="https://github.com/totti0223/stomata_quantifier/blob/master/images/overview.jpg" width="480">

## Requirements

python>3
matplotlib==1.5.1
numpy==1.11.2
scipy==0.18.1
scikit_image==0.12.3
tensorflow==0.10.0rc0
Pillow==3.2.0
common==0.1.2
cv2==1.0
dlib==19.1.0
setuptools==32.3.1

## Installation

1. Download this repository.

2. Unzip.

2. Open terminal.

3. Move to the Unzipped directory.

~~~~
pip install .
~~~~

## Note

- Tensorflow must not be ver. 1.0.. Codes are not compatible.

- Several packages such as cv2 and dlib cannot be installed via pip in anaconda environment. In such cases, comment out the requirements.txt like the following 

~~~~
#cv2 ==1.0
#dlib == 19.1.0
~~~~
and install respectively via conda install

## Usage

- In terminal

~~~~
python
import bmicp
bmicp.cui("PATH/TO/THE/DIRECTORY_OR_IMAGES")
~~~~

## Example

### 1
Analyzing a directory containing 4 jpeg images in the example folder
bmicp.cui("PATH_TO_THE_EXAMPLE_FOLDER/examples")
![ex1](https://github.com/totti0223/stomata_quantifier/blob/master/images/e1.png)

### 2
![ex1](https://github.com/totti0223/stomata_quantifier/blob/master/images/e2.png)

### 3
