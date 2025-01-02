# SolarFilamentACWE
This repository implements an ACWE-based algorithm for detecting solar filaments in H-alpha full-disk solar images. The algorithm uses a three-step process: pre-processing, segmentation, and post-processing, where deformable contours evolve based on an energy function until they reach the object boundary and minimize the energy.

**Requirements**

To run this code, you need:

* Python 3.x
* OpenCV
* Numpy
* Matplotlib

You can install the required dependencies by running:
```bash
pip install -r requirements.txt

**Important Notes**
* **Running on Local Machine:** If you are running the code on your local machine, do not use the following line:
```python

from google.colab import drive
drive.mount('/content/drive')
```
This is specifically for Google Colab. Instead, you should modify the path variables to suit your local directory structure.
* **Paths to Image and Ground Truth Folders:** You can change the paths to the image and ground truth folders according to your needs. In the code, you will find the following lines:
```
#python

image_folder = '/content/drive/MyDrive/Bulk_Filament_Detection/train/image/'
image_folder_gt = '/content/drive/MyDrive/Bulk_Filament_Detection/train/label/'
```
Modify them to point to your local or Google Drive directory depending on where you are running the code.
