# Perceptual AdEvade: Training and Evading YOLOv5-Based Ad Blocker

Nagharjun M - nm4074
Rakshana BS - rb5118
Avinash V - av3134

## Overview
AdEvade is a project focused on training a YOLOv5-based ad blocker and exploring techniques for evading detection. This includes altering test data with various ad attack methods and poisoning the training data to reduce detection efficacy.

### Repository Components
- **Scripts for Processing Images**:
  - `patchblend.py`: Applies patch blending to images.
  - `noiseadd.py`: Adds invisible noise to ad regions.
  - `resize.py`: Resizes images.
  - `adblur.py`: Applies blurring to ad regions.
  - `adblend.py`: Performs shape adjustment with inpainting.
  - `colorshift.py`: Applies color shifting to ad regions.
  - `datapoisoning.py`: Transforms training data into a poisoned version.
- **Jupyter Notebook**:
  - `adevade.ipynb`: Code for training and testing the YOLOv5 ad blocker.

## Installation

Install the necessary packages:

```bash
pip install -r requirements.txt
```

## Usage
To use the scripts for processing images, run the following commands:

### Patch Blending
```python
python patchblend.py --images_path [image_directory] \
                     --labels_path [label_directory] \
                     --target_images_path [output_image_directory] \
                     --target_labels_path [output_label_directory] \
                     --patch_fraction [desired_fraction]
```
### Noise Addition
```python
python noiseadd.py --images_path [image_directory] \
                   --labels_path [label_directory] \
                   --target_images_path [output_image_directory] \
                   --target_labels_path [output_label_directory]

```
### Image Resizing
```python
python resize.py --images_path [image_directory] \
                 --labels_path [label_directory] \
                 --target_images_path [output_image_directory] \
                 --target_labels_path [output_label_directory]

```
### Ad Blurring
```python
python adblur.py --images_path [image_directory] \
                 --labels_path [label_directory] \
                 --target_images_path [output_image_directory] \
                 --target_labels_path [output_label_directory]

```
### Ad Blending
```python
python adblend.py --images_path [image_directory] \
                  --labels_path [label_directory] \
                  --target_images_path [output_image_directory] \
                  --target_labels_path [output_label_directory]

```
### Color Shifting
```python
python colorshift.py --images_path [image_directory] \
                     --labels_path [label_directory] \
                     --target_images_path [output_image_directory] \
                     --target_labels_path [output_label_directory]

```
### Data Poisoning
```python
python datapoisoning.py --images_path [image_directory] \
                        --labels_path [label_directory] \
                        --target_images_path [output_image_directory] \
                        --target_labels_path [output_label_directory]

```

## Training and Evading the Ad Blocker
- **Training**: Use adevade.ipynb to train the YOLOv5 model.
- **Evading Techniques**:
    - Test Data Manipulation: Assess the model's detection ability under various attacks.
    - Training Data Poisoning: Introduce altered images into the training set to reduce detection efficacy.

## Results and Model Performance
<img width="468" alt="differentmetrics" src="https://github.com/Nagharjun17/Perceptual_Ad-Blocker_Evasion/assets/64778259/a666c804-9be8-41ee-a8a6-4194f280ab95">
<img width="468" alt="origvspois" src="https://github.com/Nagharjun17/Perceptual_Ad-Blocker_Evasion/assets/64778259/951f9710-62b5-4596-b9fa-8608fbb4471d">
