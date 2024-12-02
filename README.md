# Aedes-Mosquito-Image-Dataset-Version-1.0-AMID-v1
# Mpox Skin Lesion Dataset Version 2.0 (MSLD v2.0)
## Expanded Mpox Skin Lesion Dataset: 6 Distinct Classes for Robust Classification Benchmarking  

![License](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/cc.png)

The global outbreak of the virus previously called 'Monkeypox', now referred to as mpox, has caused widespread concern over the past year and continued to be a major topic in public health news headlines. During the peak transmission period back in July 2022, the World Health Organization (WHO) declared it a Public Health Emergency of International Concern (PHEIC). To obstruct its expeditious pace, early diagnosis was a must at that time. In that scenario, computer-aided monkeypox identification from skin lesion images could be a beneficial measure.

Nevertheless, no such datasets were available initially. Realizing the significance of instant release of such a dataset, we then pineered the creation of the ["Moneypox Skin Lesion Dataset (MSLD)"](https://www.kaggle.com/datasets/nafin59/monkeypox-skin-lesion-dataset) by collecting and processing 'monkeypox' and 'non-monkeypox' (measles, chickenpox)images from different means of web-scrapping i.e., from news portals, websites and publicly accessible case reports. Now that the cases have come under control, ensuring the clinical soundness of the data through expert verification and feedback incorporation is crucial for developing effective algorithms to tackle any future cases of monkeypox or diseases with similar skin lesions. Therefore, we introduce an updated version, ["Mpox Skin Lesion Dataset Version 2.0 (MSLD v2.0)"](https://www.kaggle.com/datasets/joydippaul/mpox-skin-lesion-dataset-version-20-msld-v20). Instead of placing the non-mpox cases in a single class, we have added definite class labels such as, chickenpox, measles, cowpox, hand-foot-mouth disease, and healthy. 


<!--The recent monkeypox outbreak has become a global healthcare concern owing to its rapid spread in more than 65 countries around the globe.  But the confirmatory Polymerase Chain Reaction (PCR) tests and other biochemical assays are not readily available in suffiecient quantities. --> <br />

Graphical representation of our intended working pipeline:<br />


![Working pipeline](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset-v2/blob/main/Assets/GA_aug.JPG)

* * *

# Contents

This repository gives access to the Mpox Skin Lesion Dataset Version 2.0 (MSLD v2.0). The creation of this dataset is primarily focused on distinguishing the monkeypox cases from the similar non-monkeypox cases. Therefore, along with the 'Monkeypox' class, we included skin lesion images of 4 other disease classes (and the healthy class) because of their resemblance to the monkeypox rash and pustules in initial state. These classes can be put together in to perform binary classification or we can use them for performing differential diagnosis via multi-class classification.<br />

The dataset itself is available for download at the [Kaggle](https://www.kaggle.com/datasets/joydippaul/mpox-skin-lesion-dataset-version-20-msld-v20) or the [Google Drive](https://drive.google.com/drive/folders/1_bGmbDQNgJViQenjZ4QUhhzpdiubga48?usp=sharing).<br />


Some sample images from the dataset:<br />


![Sample Images](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset-v2/blob/main/Assets/samples.jpg)


* * *

# Dataset Description
The dataset contains a total number of 755 images from 541 unique patients. The class distribution is presented as follows:

| Class label                    | No. of Original Images | No. of Unique Patients |
|-------------------------------|-----------------------|------------------------|
| Mpox                          | 284                   | 143                    |
| Chickenpox                    | 75                    | 62                     |
| Measles                       | 55                    | 46                     |
| Cowpox                        | 66                    | 41                     |
| Hand, foot and mouth disease  | 161                   | 144                    |
| Healthy                       | 114                   | 105                    |
| Total                         | 755                   | 54                     |



There are 2 folders in the dataset.<br />

1) Original Images: This folder includes a subfolder named "FOLDS" containing five folds (fold1-fold5) for 5-fold cross-validation with the original images. Each fold has separate folders for the test, train, and validation sets.<br />

2) Augmented Images: To aid the classification task, several data augmentation methods such as rotation, translation, reflection, shear, hue, saturation, contrast and brightness jitter, noise, scaling etc. have been applied using MATLAB R2020a. Although this can be readily done using ImageGenerator/other image augmentors, to ensure reproducibility of the results, the augmented images are provided in this folder. It contains a subfolder called "FOLDS_AUG" with augmented images of the train sets from each fold in the "FOLDS" subfolder of the "Original Images".***The augmentation process resulted in an approximate 14-fold increase in the number of images.***<br />
 

### Naming Convention of the Images
Each image is assigned a name following the format of ***DiseaseCode_PatientNumber_ImageNumber***. The corresponding disease codes assigned to each of the ***six disease classes*** are - **Mpox -> MKP, Chickenpox -> CHP, Cowpox -> CWP, Measles -> MSL, Hand,foot and mouth disease -> HFMD, Healthy -> HEALTHY**. Assignment of the keywords is illustrated in the provided image "Keywords.jpg". For instance, an image named "MKP_17_01" indicates that it belongs to the Mpox class and is the first image captured from a patient with the ID 17.

### Data Organization
The dataset includes an Excel file named ***"datalog.xlsx"*** consisting of 5 sheets (Sheet1-5), with each sheet corresponding to a specific fold (fold1-5). Each sheet contains three columns: train, validation, and test. These columns contain the names of the images belonging to the respective train, validation, and test sets for a particular fold.


<!-- ![Data Preparation](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/data_split.png)-->

* * *
# Provenance

### Sources
In the acquisition of images for MSLD v2.0, the same technique as in the previous version was employed, utilizing web-scraping to gather skin lesion images belonging to the six classes. Automated web-scrappers have not been used for ensuring image quality and data label. The dataset was constructed by sourcing images from reputable and reliable online platforms, including trusted news portals, websites, and academic journals. Each image was meticulously recorded along with its respective source information to facilitate further verification and ensure proper attribution. Copyright considerations were duly addressed, adhering to appropriate protocols to safeguard intellectual property rights.

### Collection Methodology
In MSLD v2.0, a two-fold verification process was implemented to ensure the quality and reliability of the acquired skin lesion images. The first step was verification via Reverse Image Search. This technique of verification via reverse image search is similar to the one employed in MSLD v1.0. This involved conducting a comprehensive reverse image search using tools such as Google's Reverse Image Search. By cross-referencing the sources of the images with reputable platforms such as journals and renowned websites, the authenticity and credibility of each image were examined. This rigorous verification process ensured that only images with verified and trustworthy sources were included in the dataset. The second step was Verification by a Professional Dermatologist. In MSLD v2.0, a professional dermatologist played a crucial role in the verification process. Each image was carefully scrutinized by the dermatologist to ensure its accuracy and reliability. Any images that were difficult to understand or had mislabeling were eliminated from the dataset.

* * *
<!-- !# Sample Notebook for Classification

To see, how you can use this dataset for performing binary classification, please refer to the following notebooks:<br />
- [Notebook1](https://www.kaggle.com/code/gpiosenka/monkey-pox-f1-score-90) <br />
- [Notebook2](https://www.kaggle.com/code/nafin59/monkeypox-sample-classification-notebook)<br />-->

* * *

# Web-Application

Since we intend to build an end to end solution - starting with dataset creation and ending with a live web app, a prototype of the web-app has already been developed using the open-source python streamlit framework with a flask core and has been hosted in the streamlit provided server for better user experience. In the app, [Skin Lesion Detector](https://skinlesionclassifierbymhealthlab.streamlit.app/), users can get, not only a suggestion but also the accuracy of the suggestion. <br />

The codes required to build and train the model, all the javascript, css and html files as well as the trained model will be made opem-source soon. The app's dynamic and future updates will incorporate the ability to store user data and use them to train the model realtime.<br />

![Sample Images](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset-v2/blob/main/Assets/app_int_dark.png)

* * *

# Citation

If this dataset helped your research, please cite the following [papers](https://arxiv.org/abs/2207.03342):<br />

Ahmed, M. T., Paul, J., Jahan, T., Ali, S. N., Sani,  S. M. Sakeef, Noor, N., Asma, A. N., & Hasan, T. (2023). Monkeypox Skin Lesion Detection Using Deep Learning Models: A Preliminary Feasibility Study. arXiv preprint arXiv:xxxx.xxxxx.

>@article{Ahmed2023,<br />
  title={A Study on Mpox Skin Lesion Detection Using State-of-the-art Deep Learning Models},<br />
  author={Ahmed, Md. Tazuddin and Paul, Joydip  and Jahan, Tasnim and Ali, Shams Nafisa and Sani,  S. M. Sakeef and Noor, Nawshaba and Asma,     Anzirun Nahar and Hasan, Taufiq},<br />
  journal={arXiv preprint arXiv:xxxx.xxxxx},<br />
  year={2023}<br />
}

Ali, S. N., Ahmed, M. T., Jahan, T., Paul, J., Sani, S. M. Sakeef, Noor, N., Asma, A. N., & Hasan, T. (2024). [A Web-based Mpox Skin Lesion Detection System Using State-of-the-art Deep Learning Models Considering Racial Diversity.](https://doi.org/10.1016/j.bspc.2024.106742) Biomedical Signal Processing and Control, 98, 106742.

>@article{Ali2024,<br />
  title={A Web-based Mpox Skin Lesion Detection System Using State-of-the-art Deep Learning Models Considering Racial Diversity},<br />
  author={Ahmed, Md. Tazuddin and Paul, Joydip  and Jahan, Tasnim and Ali, Shams Nafisa and Sani,  S. M. Sakeef and Noor, Nawshaba and Asma,     Anzirun Nahar and Hasan, Taufiq},<br />
  journal={Biomedical Signal Processing and Control},<br />
  volume={98},<br />
  pages={106742},<br />
  year={2024},<br />
  publisher={Elsevier}<br />
}
## Aedes Mosquito Image Dataset Version 1.0 (AMID v1.0)
## Introduction
The outbreak of dengue fever in recent years has become a grave public health concern as it has spread to 20 countries in South America and South Asia. As vectors of the flavivirus, several mosquito species belonging to the Aedes genus are responsible for transmitting dengue fever. Effective vector surveillance and control are essential in reducing dengue outbreaks. However, due to their minute variations in anatomical structure, it is challenging to identify Aedes mosquitoes without expert entomologists using a microscope. In this regard, deep learning algorithms can play a vital role in identifying mosquitoes using smartphone-captured images and pave the way for deskilling automated vector surveillance, provided that sufficient training examples are available. 

A graphical representation of our working pipeline:
![](https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F15444916%2F19a5be5f62e8c13d80e4eeb60f83b5c9%2FA%20flow-diagram%20of%20the%20proposed%20mosquito%20detection%20system.png?generation=1718534243741585&alt=media)

## Contents
In this study, we developed the “Aedes Mosquito Image Dataset,” consisting of smartphone-captured mosquito images consisting of 8 class labels: Aedes aegypti, Aedes koreicus, Aedes albopictus, Culex pipiens, Armigeres subalbatus, Culex quinquifasciatus, Aedes japonicus, and others (non-mosquito). The images are collected by trapping mosquitoes in several locations in Dhaka, followed by image capture and expert annotations in collaboration with ICDDR,B. Additional image data is collected from open-access online repositories. 

Some sample images from dataset: 
![](https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F15444916%2F95a785845e1d50ee6fc90683c1dbe58b%2FDifferent%20types%20of%20Mosquito%20Species.png?generation=1718537439037243&alt=media)

## Dataset Description
The dataset contains a total of 31999 images from 3 sources. The class distribution is presented as follows:
| Class label                     | No. of Images from Mosquito Alert | No. of Images from ICDDR,B | No. of Images from WHO | Total No. of Images (Class label Wise) |
|---------------------------------|-----------------------------------|----------------------------|-------------------------|----------------------------------------|
| *Aedes aegypti*                   | 73                                | 247                        | 499                     | **819**                                    |
| *Aedes albopictus*                | 15,268                            | 7                          | 500                     | **15,775**                                 |
| *Aedes japonicus*                 | 153                               | 0                          | 0                       | **153**                                    |
| *Aedes koreicus*                  | 38                                | 0                          | 0                       | **38**                                     |
| *Armigeres subalbatus*            | 0                                 | 42                         | 0                       | **42**                                     |
| *Culex pipiens*                   | 6,180                             | 231                        | 0                       | **6,411**                                  |
| *Culex quinquefasciatus*          | 0                                 | 0                          | 500                     | **500**                                    |
| Others (non-mosquito)           | 8,261                             | 0                          | 0                       | **8,261**                                  |
| **Total No. of Images (Source Wise)** | **29,973**                       | **527**                    | **1,499**               | **31,999**                             |


This dataset has 8 subfolders, which contain 7 kinds of mosquito images and 1 folder (other_species) for non-mosquito images.

## Source
The dataset was constructed by sourcing images from [Mosquito Alert](https://www.mosquitoalert.com/en/mosquito-images-dataset/), [WHO accredited breeding laboratory](https://data.mendeley.com/datasets/zw4p9kj6nt/2) & Trap set up by ICDDR,B. Each image was meticulously recorded along with its respective source information to facilitate further verification and ensure proper attribution. Copyright considerations were duly addressed, adhering to appropriate protocols to safeguard intellectual property rights.

## Naming Convention of the Images
Each image is assigned a name following the format of SourceCode_ClassLabel_Cropped_CroppingNumber_Resized. The corresponding source codes assigned to each source are: Mosquito Alert -&gt; MSA; ICDDR,B -&gt; ICD; WHO accredited breeding laboratory -&gt; WHO. For instance, an image named "ICD_Aedes_aegypti_Cropped_239_Resized" indicates that it was collected from ICDDR,B, belongs to the *Aedes aegypti* class, cropped using YOLO, cropping id was 239 & finally it was resized to 256 by 256.

##Collection Methodology
In AMID v1.0, our mosquito images are collected by setting up traps in various locations within ICDDR,B, Bangladesh University of Engineering and Technology (BUET) and University of Dhaka (DU). We utilized BG-Sentinel traps containing human sweat extract that attracted Aedes mosquitoes. Additional mosquito image samples were collected from the open-access dataset “Mosquito Alert" and images provided by WHO accredited breeding laboratory. We did not use any automatic web scrapers. In this work, we mainly focus on distinguishing Aedes mosquitoes like *Aedes aegypti, Aedes koreicus, Aedes albopictus,* and *Aedes japonicus* from other mosquito species. Entomologists in ICDDR,B and the entomology department at the University of Dhaka properly verified & labeled all the images of mosquitoes. Through a two-step screening process, out of focus, low-resolution images devoid of mosquito information and low-quality images are discarded, and only the unique images that meet the quality requirements are selected. Next, the images were cropped according to the region of interest by the YOLO model and resized to 256 × 256 pixels, maintaining the aspect ratio. 

##Web-Application
A web app prototype has already been created using the open-source Python streamlit framework with a flask core, and it has been hosted on the streamlit server for an improved user experience, since our goal is to create an end-to-end solution that begins with dataset creation and ends with a live web application. 

![](https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F15444916%2Fca284bf98d369ee44636315f7fadb92f%2FThe%20interface%20of%20the%20online%20Mosquito%20detection%20tool..png?generation=1718540026545051&alt=media)
