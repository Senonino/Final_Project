<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# Arabic-Handwritten-Characters-Recognition using ResNet-50

*Senan Jadeed*

*Ironhack Data Analytics BootCamp (Jan-Mar).2020, Berlin*

## Content

- [Project Description](#project-description)
- [Questions & Hypotheses](#questions-hypotheses)
- [Final Results](#Final-Results)
- [Repository contents](#Repository-contents)
- [Links](#links)

## Project Description

### You can get this [dataset](https://www.kaggle.com/rashwan/arabic-chars-mnist) from kaggle website

Arabic Letters Dataset is composed of 16,800 characters written by 60 participants, the age range is between 19 to 40 years, and 90% of participants are right-hand. Each participant wrote each character (from ’alef’ to ’yeh’) ten times. The images were scanned at the resolution of 300 dpi. Each block is segmented automatically using Matlab 2016a to determining the coordinates for each block. The dataset is partitioned into two sets: a training set of 13,440 characters to 480 images per class and a test set of 3,360 characters to 120 images per class. Writers of the training set and test set are exclusive. Ordering of including writers to test set are randomized to make sure that writers of the test set are not from a single institution to ensure variability of the test set.

`ResNet-50` is a convolutional neural network that is trained on more than a million images from the ImageNet database. The network is 50 layers deep and can classify images into 1000 object categories, such as keyboard, mouse, pencil, and many animals. As a result, the network has learned rich feature representations for a wide range of images. The network has an image input size of 224-by-224, [Source](https://www.mathworks.com/help/deeplearning/ref/resnet50.html).

#### Citation
> Ahmed El-Sawy, Mohamed Loey, Hazem EL-Bakry, and their paper "Arabic Handwritten Characters Recognition using Convolutional Neural Network, WSEAS, 2017".

I had no role in constructing the original images and all the credit goes to the original authors of the [dataset](https://www.kaggle.com/mloey1/ahcd1/home) Ahmed El-Sawy, Mohamed Loey, Hazem EL-Bakry, and their paper "Arabic Handwritten Characters Recognition using Convolutional Neural Network, WSEAS, 2017". The original dataset has the images as an array of size (32,32,1) this dataset only converts the arrays to their respective jpg images.

The Main notebook is using a pre-trained ResNet-50 from Pytorch models and using the Fast.AI library which makes the training and validation super easy and fast.

#### Acknowledgement

All credit goes for the original authors of this dataset who made available a great dataset that is essential for anyone looking into Arabic character recognition and I hope to see more like it in other fields of the Arabic literature.

## Questions & Hypotheses

The Arabic language has many fonts and ways of writings. The idea behind this project is to develop a model that can predict the different handwriting styles, which is highly difficult as the cursive writing styles makes it nearly undetectable to the trained human eye in some occasions.
In my approach, I use the same basic steps of image processing introduced by the Fast.AI authors, and in the last stage, I fine-tune the parameters utilizing the Fast.AI library capabilities. Therefore, able to achieve an accuracy of 98.74%, which is a vast improvement from the highest registered accuracy score I am able to find in any official paper (97.3%) as shown in the final results section.
After the analysis was finished and I tested the model against a small dataset that I wrote, I concluded that a better dataset with more extensive writing styles is needed in order to cover more possible scenarios where the letters are not easily unrecognizable.

## Final Results

A comparison between the literature and the two models I tested is shown in the table below:

| Publication's title|Authors|Accuracy achieved|Date of publication |
|--------------------|------|----------------|--------------------|
|High Accuracy Arabic Handwritten Characters Recognition Using Error Back Propagation Artificial Neural Networks|Assist. Prof. Majida Ali Abed & Assist. Prof. Dr. Hamid Ali Abed Alasad|93.61%|February 2015|
| Convolutional Neural Network Model for Arabic Handwritten Characters Recognition|Murtada Khalafallah Elbashir & Mohamed Elhafiz Mustafa|93.5% | November 2018 |
| ARABIC HANDWRITTEN CHARACTER RECOGNITION BASED ON DEEP CONVOLUTIONAL NEURAL NETWORKS | Khaled S. Younis | 97.6% | December 2017 |
| Arabic-Handwritten-Characters-Recognition using CNN_ResNet-18 | Senan Jadeed | 97.23% | March 2020 |
| Arabic-Handwritten-Characters-Recognition using CNN_ResNet-50 | Senan Jadeed | 97.95% | March 2020 |

The final results show that with the basic model using ResNet-18, the accuracy achieved is comparable to the highest accuracy achieved using the previously reported methods in the literature.
By using ResNet-50 the accuracy achieved is much higher 98.74%. By putting the model to test by using it on my handwriting, the assumption made is that the quality of the dataset used is not high enough, so with a better dataset higher accuracies when tested against external datasets could be anticipated.

## Repository contents

- Data folder that contains the dataset used and the models produced.
- Extra folder that contains the content used in preparing the presentation, the presentation pdf file and the dataset used in win.rar format.
- ShowTest folder that contains the small dataset I created to test the models produced.
- Jupyter notebooks that were used in producing the models and another notebook used in testing the models.

## Links

[Final Project Repository](https://github.com/Senonino/Final_Project)

[Google Slides](https://github.com/Senonino/Final_Project/blob/master/Extras/Arabic%20Handwritten%20Recognition%20Presentation.pdf)

For more info please feel free to contact me via [E-mail](eng.jadeed@gmail.com).
