# Melanoma Detection Assignment
> Assignment to build a CNN based model which can accurately detect melanoma.


## Table of Contents :
* [Problem Statement](#problem-statement)
* [Objectives](#objectives)
* [Approach](#approach)
* [Technologies/Libraries Used](#technologies/libraries-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
* [Glossary](#glossary)
* [Author](#author)


## Problem Statement
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


You can download the dataset [here](https://drive.google.com/file/d/1xLfSQUGDl8ezNNbUkpuHOYvSpTyxVhCs/view)


The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:

- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion 

 NOTE:

- Should not use any pre-trained model using Transfer learning. All the model building processes should be based on a custom model.
- Some of the elements introduced in the assignment are new, but proper steps have been taken to ensure smooth learning. 
- The model training may take time to train as you will be working with large epochs. It is advised to use GPU runtime in Google Colab.
 ## Objectives
The primary objective of this assignment is to develop a custom convolutional neural network (CNN) model capable of accurately classifying images of various skin lesions, specifically focusing on melanoma detection. The model aims to enhance early diagnosis and provide a reliable tool for dermatologists by automating the analysis of skin images, thereby potentially reducing the manual effort involved in identifying melanoma and other oncological diseases. Additionally, the assignment seeks to explore different model architectures and optimization techniques to improve classification accuracy and robustness.

## Approach

- Step 1: Import Necessary Libraries
- Step 2: Load the Data and Understanding the Data
- Step 3: Data Preparation Steps - Train-Validation Split and Test Set
- Step 4: Building the Initial Model (Model 1)
- Step 5: Data Augmentation - Build Model after Applying Augmentation
- Step 6: Fix Class Imbalance and Build the Model
- Step 7: Fine-tune and Optimize the Model
- Step 8: Making Predictions Using the Models
- Step 9: Conclusion
  
## Technologies/Libraries Used
- numpy : 1.26.4
- pandas : 2.2.2
- matplotlib : 3.7.1
- tensorflow : 2.17.0
- keras : 3.4.1
- augmentor : 0.2.12

## Conclusions
**Based on the model comparison and evaluation, the following insights can be drawn: -**
- Model 8 (Base Model + Augmented Layers + Balanced Class + Controlled LR + More Layers + Less Dropouts) achieved the best overall performance with the highest validation accuracy (0.68) and test accuracy (0.47). This suggests that optimizing dropout rates and balancing the class distribution improves model generalization.
- Model 4 (Base Model + Augmented Layers + Balanced Class + Controlled LR) and Model 5 (Base Model + Augmented Layers + Balanced Class + Increased / Controlled LR) both show competitive results, with test accuracies of 0.43. These models effectively address class imbalance and fine-tune the learning rate.
- Model 6 (Base Model + Augmented Layers + Balanced Class + Controlled LR + More Epochs) achieved better training accuracy (0.65) but slightly lower test accuracy (0.42), indicating potential overfitting as the model learned too well on the training data.
- Base Models (1, 2, 3) show lower test accuracies, especially Model 1 which had high training accuracy (0.84) but low generalization on the test set (0.31), demonstrating severe overfitting without any regularization techniques.
- Overall, applying data augmentation, class balancing, learning rate control, dropout optimization, and deeper architectures significantly enhanced the performance of the CNN models for melanoma detection, with Model 8 emerging as the most balanced in terms of validation and test performance. Further optimization could continue to improve this performance.

**Q :- Which class has the least number of samples?
Answer - seborrheic keratosis has the least number of samples - 77
**Q :- Which classes dominate the data in terms proportionate number of samples?
Answer - pigmented benign keratosis dominates the data in terms proportionate number of samples - 462



## Acknowledgements

- The project reference course materieals from upGrads curriculm .
- The project references from presentation in upgrad live class given by [Shivam Garg]( https://www.linkedin.com/in/shivam-garg-0494a2ab )
- The project references insights and inferences from presentation in upgrad live class given by [Akashdeep Makkar]( https://www.linkedin.com/in/akashdeep-makkar-12110880/ )

## Glossary

- Data Augmentation
- Class Imbalance
- Train-Validation Split
- Test Set
- Convolutional Neural Network (CNN)
- Dropout
- Learning Rate (LR)
- Overfitting
- Early Stopping
- Cross-Entropy Loss
- Accuracy
- Batch Normalization
- Max Pooling
- Softmax
- Learning Rate Scheduler (ReduceLROnPlateau)

## Author
* [Arnab Bera]( https://www.linkedin.com/in/arnabbera1994/ )
