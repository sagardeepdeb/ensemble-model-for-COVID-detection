# Ensemble DCNN structure for detection of COVID-19 from Chest X-Ray images
This notebook will detect COVID-19 from Chest X-Ray images
The year 2020 will certainly be remembered for the COVID-19 outbreak. First reported in Wuhan city of China back in December 2019, the number of people getting affected by this contagious virus has grown exponentially. Every country in this world been affected by this highly infectious disease.Shortage of testing kits and increasing number of fresh cases encouraged us to come up with a model that can aid radiologists in detecting COVID19 using chest X-ray images. With RT-PCR being the gold standard screening method and its time consuming nature, we aim to propose a real time model for detection of COVID19. 
Researchers all around the world are working day and night to counter this pandemic. Researchers of image processing and bio-medical engineering fields are also not left behind.
Our ensemble model aims to classify the input Chest X-Ray into three classes namely- Community Acquired Pneumonia (CAP), Normal and COVID-19. In the beginning, individual DCNN structures are used for feature extraction, which are provided into a fully connected layer for classification task. Later on we have used the ensemble of the four most common DCNN structures for feature extraction. As shown in figure 1, the low level features from the input images are extracted using an ensemble of the four pre-trained DCNNs. The details of the feature length and the architecture are given in table 1. We have observed that employing such design enhances the classification performance. A brief description of all the four DCNNs structures are given below.

![Figure 1](https://github.com/sagardeepdeb/ensemble-model-for-COVID-detection/blob/master/model.PNG)


Comparision between the performance of the individual DCNN structures along with that of our ensemble model is given below

Architecture | Performance
------------ | -------------
VGG | 87.23
GoogleNet | 86.78
DenseNet | 85.67
NASNet | 83.23
_Our model_ | 88.92


The confusion matrix for the same is given below

![Figure 1](https://github.com/sagardeepdeb/ensemble-model-for-COVID-detection/blob/master/confusion_marix.png)

The same problem was extended for binary class classification. The following measures are collected for binary classification.


Class        |	Precision (%)	|  Recall(%) | F-measure(\%)
------------ | ---------------| ---------- | -------------
COVID-19     |     87.41      |    97.05   |    91.97 	
NonCOVID-19  |     99.72      |    98.74   |    99.23
