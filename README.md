# COVID-19 CT Scan Lesion Segmentation (Short Doc)
## _Muhammad Shariq Shoaib MSCSF21M507_

A semester project for the course of
Deep Learning CS-568


## Abstract

Image Processing has been always considered as top ranked research areas in Computer Sciences. Where Medical Image Processing/Analysis is among the key research topics as there are infinite problems relevant to medical domains that requires the fast computational power to help in order to save lives. In this project the goal is to design a lesion segmentation system by using a dataset of Lungs CT scans having lesions in Covid-19.
Dataset consists of 2729 CT-scan image and ground truth mask pairs. All types of lesions are mapped to white color in the ground truth for consistency across dataset. This project will be done in incremental phases, where firstly I’ll be considering for
such pre-processing techniques which result in highlighting lesions region the most .
In the second phase, I’ll be looking forward for segmenting the lesion and comparing
different techniques for segmenting in order to achieve better results.
If these phases are done well before time and I’ll be comparing other researchers’ methodology and improve further.


Dataset Source:
https://www.kaggle.com/maedemaftouni/covid19-ct-scan-lesion-segmentation-dataset
Keywords: Image Processing; Medical Image Analysis; Covid-19; CT Scan; Lesion; Segmentation; Ground Truth;

APEER - Labeling tool
Code Help Source: https://github.com/bnsreenu/python_for_image_processing_APEER/blob/master/tutorial117_building_unet_using_encoder_decoder_blocks.ipynb

## Introduction
A unexpected outbreak of the rare respiratory disease was reported in Wuhan, China,
near the end of December 2019. The Chinese Center for Disease Control and Prevention examined the lower respiratory tracts of sick patients and discovered COVID19, a novel coronavirus. COVID-19 is a systemic infection that primarily affects the
endothelium layer of the lungs and spreads from person to person, whether symptomatic or asymptomatic.
Post-COVID-19 pulmonary fibrosis is characterised as the occurrence of fibrotic
CT alterations on follow-up studies that are commonly clinically associated with
decreased lung function. Even though histopathological patterns in post-COVID-19
pulmonary fibrosis have yet to be discovered, they are thought to be those of an
organising and fibrotic phase of diffuse alveolar damage (DAD), fibrosing nonspecific
interstitial pneumonitis, and organizing pneumonia. CT features being potentially
identified in pulmonary fibrosis secondary to COVID-19 pneumonia have been suggested to include the presence of architectural distortion, reticular lesions, traction
bronchiolectasis, ground-glass opacity, mosaic attenuation, and honeycombing in
consideration of presumed histopathologic patterns. But according to the study
by Pan et al (1), the CT features seen at one-year follow-up studies were those of
fibrotic-like linear or multifocal reticular and/or cystic lesions.
There were no typical CT DAD findings, such as fibrosing nonspecific interstitial pneumonitis or organised pneumonia patterns. Follow-up CT characteristics
of severe acute respiratory syndrome-associated coronavirus (SARS-CoV) infection
produced comparable results. Patients with underlying interstitial lung disease, particularly those with poor lung function and obesity, are at a higher risk of death
from COVID-19.
Finally, follow-up CT scans of COVID-19 pneumonia patients reveal persistent
fibrotic-like linear or multifocal reticular/cystic lesions. So if we segment the lesion region, it’ll be helpful for post COVID treatment by looking at the affected
areas of lungs.


##  Literature Review
1. Lung Lesion Segmentation Using Gaussian Filter and Discrete Wavelet
Transform
By Kamil Dimililer, Ali Hesri and Yoney Kirsal Ever
( 10.1051/itmconf/20171101018 )
1 Electric and Electronic Engineering Department, Near East University, North Cyprus, Mersin 10 Turkey
2 Software Engineering Department, Near East University, North Cyprus, Mersin 10 Turkey
Lesions inside the lungs are called a great early symptom for detection of
Lung cancer. Lung cancer is a growing tumour that are cells covering the
airways of the major respiratory system.
Here they’ve used CT scans and applied image processing different applications and investigated the effectiveness of different types of discrete wavelets
to obtain accurate results.
Haar Wavelet, Db7 and Bi-orthogonal wavelet are being used along with Median and Gaussian Kernels.
2. COVID-19 Lesion Segmentation Using Lung CT Scan Images: Comparative Study Based on Active Contour Models
By Younes Akbari, Hanadi Hassen, Somaya Al-Maadeed and Susu M.Zughaier
( https://doi.org/10.3390/app11178039 )
1 Department of Computer Science and Engineering, Qatar University, Doha 122104, Qatar
2 College of Medicine, QU Health, Qatar University, Doha 122104, Qatar
Pneumonia being a lung infection is highly threatening. COVID-19 causing
pneumonia is being segmented here using CT scans to find how effective Active
Contour Models (ACM) are. This research provides the basis on which further
ACM related Lung Segmentation can be done in the COVID-19 domain.
They’ve shown how initially contour results and improvements in result if
(Gac, C-V, MAC, Lsacm, Frbacm) Models of Active Contour are used.
3. Dual-branch combination network (DCN): Towards accurate diagnosis and lesion segmentation of COVID-19 using CT images
By Kai Gao, Jianpo Su, Zhongbiao Jiang et al.
( https://doi.org/10.1016/j.media.2020.101836 )
1 College of Intelligence Science and Technology, National University of Defense Technology, Changsha,
Hunan, China
2 Department of Radiology, Third Xiangya Hospital, Central South University, Changsha, Hunan, China
3 Department of Radiology, Second Xiangya Hospital, Central South University, Changsha, Hunan, China College of Computer Science and Technology, National University of Defense Technology, Changsha, Hunan, China
As the COVID-19 outbroke from Wuhan China and as a result, many different diagnostic tools were developed, CT(computer tomography)-based diagnostic tool faced further complications due to lack of adequate manuallydelineated samples. So dual-branch combination network (DCN) was developed to achieve classification and lesion segmentation which resulted in high
accuracy. CT scan images are preprocessed first using U-net and then DCN
is applied which uses FC Net to get lesion segmentation.
4. Lung Lesion Detection in CT Scan Images Using the Fuzzy Local
Information Cluster Means (FLICM) Automatic Segmentation Algorithm and Back Propagation Network Classification
By M Lavanya and P Muthu Kannan
( https://dx.doi.org/10.22034%2FAPJCP.2017.18.12.3395 )
1 Department of Electrical and Electronics Engineering, Saveetha School of Engineering, Saveetha University, Thandalam, Chennai-602 105, India.
Lungs’ cancer has always been a deadly and diagnostic method for lung tumours that weren’t up to the mark then due to variation in lesions. These
researchers proposed a segmentation technique using the FLI Cluster Mean
algorithm for segmentation and further clustering is done to achieve accurate
results after which Edge detection was done to extract features and Classification is achieved using Back Propagation Network.
It resulted in far better accuracy than existing methods of that time.

5. Dense GAN and multi-layer attention based lesion segmentation
method for COVID-19 CT images By Ju Zhang, Lunduan Yu at el.
( https://doi.org/10.1016/j.bspc.2021.102901 )
1 Zhijiang College of Zhejiang University of Technology, Shaoxing 312030, China
2 College of Computer Science and Technology Zhejiang University of Technology, Hangzhou 310023, China
3 College of Information Engineering, Zhejiang University of Technology, Hangzhou 310023, China
4 Department of Medical Imaging, Zhejiang Hospital, Hangzhou 310013, China
Testing and screening during COVID-19 pandemic was a headache for governments. AS CT-scan images were clear diagnostic medium, medical imaging
researchers proposed a technique in which novel Dense GAN was developed to
get clear images and U-NET combined with multi-layer attention mechanism
was used to get accurate lesion segmentation. Further related work resulted
in Dense Generative Adversarial Network(DGAN)
Precision by this proposed method was as high up to 0.94.

## Framework
Tensorflow Keras, Numpy, Matplotlib and other  dependencies

## Methodology
### 1 Pre-processing
Due to the limitation of hardware resources, and time, No preprocessing was
done and all images are fed as they were collected

### 2 Model Selection
Currently, I have used U-Net with the attention model having following details.
Again due to hardware limitation 851 unique images were selected to train our
DL model (U-Net) as it allows to have a versatile boundary.

11 hidden layers
Total params: 31,117,985
Trainable params: 31,105,953
Non-trainable params: 12,032
### 3 Evaluation
Intersection over union IoU has been used as the evaluation metric. And for training accuracy was being calculated at each epoch.

##  Results
Data was divided into 80 percent training and 20 percent testing and by UNet
with attention model we achieved IoU of 0.60990273 on the pixel based resulting in form of mask. Predicted masks are attached in the PDF report attached(DL_Project_MSCSF21M507.pdf) in current directory.
