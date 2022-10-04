# EsophagealCancerSegmentation
A pretrained nnU-Net model based on contrast-enhanced CT images.

# 1 Requirements
torch>1.10.0

install or download nnU-Net which is available at https://github.com/MIC-DKFZ/nnUNet
# 2 How to use the pretrained model for esophageal cancer segmentation
Once the nnU-Net was installed, the above Task067_EsophagealCancer folder should be placed in "xxx/nnUNet_trained_models/nnUNet/3d_fullres/", and then run the predict_simple.py file from nnU-Net.
```
python predict_simple.py -i InputFolder -o OutputFolder -t 67 -f 0 -m 3d_fullres
```
# 3 The training and validation details
The pretrained model was trained based on contrast-enhanced CT images from 120 patients with esophageal cancer, and validated on CT images from 30 EC patients.

The training progress is shown as the following figure
![progress](https://user-images.githubusercontent.com/79628308/192688658-20c31f6a-3e8c-4a76-babc-77d8cedb7763.png)

On two independent test datasets (n = 33 and 55), the pretrained model achieved a dice coefficient of 0.798 (std: 0.106) and 0.829 (std: 0.057).

# 4 Citation
```
Isensee, Fabian, Paul F. Jaeger, Simon AA Kohl, Jens Petersen, and Klaus H. Maier-Hein. "nnU-Net: a self-configuring method for deep learning-based biomedical image segmentation." Nature methods 18, no. 2 (2021): 203-211.
```
