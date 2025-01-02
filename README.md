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
```

**Important Notes**
* **Running on Local Machine:** If you are running the code on your local machine, do not use the following line:
```python

from google.colab import drive
drive.mount('/content/drive')
```
This is specifically for Google Colab. Instead, you should modify the path variables to suit your local directory structure.
* **Paths to Image and Ground Truth Folders:** You can change the paths to the image and ground truth folders according to your needs. In the code, you will find the following lines:
```python

image_folder = '/content/drive/MyDrive/Bulk_Filament_Detection/train/image/'
image_folder_gt = '/content/drive/MyDrive/Bulk_Filament_Detection/train/label/'
```
Modify them to point to your local or Google Drive directory depending on where you are running the code.
* File Formats: The input solar images should be in .jpg, .jpeg, or .png format. You can download such images from this [link](https://sun10.bao.ac.cn/hsos_data/download/filaments-unet-dataset/img/).
* Ground Truth: If you want to compare the results with the ground truth, you can download the ground truth images from [here](https://sun10.bao.ac.cn/hsos_data/download/filaments-unet-dataset/mask/).
* Displaying Images: If you are running the code on your local machine, use cv2.imshow to display images. For Google Colab, the code uses cv2_imshow to display images inline. Modify it based on your environment.

**Citation**

If you are using the solar image dataset from this source [https://sun10.bao.ac.cn/hsos_data/download/filaments-unet-dataset/](https://sun10.bao.ac.cn/hsos_data/download/filaments-unet-dataset/), please cite the following paper:
```
Zhu, G., Lin, G., Wang, D. et al. Solar Filament Recognition Based on Deep Learning. Sol Phys 294, 117 (2019). https://doi.org/10.1007/s11207-019-1517-4
```
If you are using this code, please cite:
```
S. Bandyopadhyay and V. Pant, "Solar Filaments Detection using Active Contours Without Edges," 2024 URSI Regional Conference on Radio Science ( URSI-RCRS), Bhimtal, India, 2024, pp. 1-4, doi:10.46620/URSI_RSRC24/0449KIA7088.
```

**Acknowledgements**

Additionally, **whoever is using the code** is requested to acknowledge the source of the data as:
***"The author/authors thankfully acknowledge the use of code courtesy of the Aditya-L1 Support Cell Team."***
