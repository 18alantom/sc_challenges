# sc_challenges
Notebooks and files containing attempts at the Skill Connect Challenges

___

# Week 2 challenges 
## Self Developed Architecture
**Dataset**
[CIFAR10](https://www.tensorflow.org/api_docs/python/tf/keras/datasets/cifar10/load_data)
A dataset of 60k images having 10 classes, 50k for training and 10k for validation.

**Architecture**
- Coded a small arcitecture *LameNet* in pytorch and keras to get more familiar with both the libraries.
- The architecture makes use of concepts from *Inception* (a simple inception module) and *Resnets* (skip connections).
- Managed an accuracy of 77.82 % using pytorch in 30 epochs and 74.61 % using keras in 33 epochs (Early Stopping)
- [COLAB](https://colab.research.google.com/drive/15oDlv8jTjr8f11UuenMCF9ZoDZxlP2JW)

## Transfer Learning
**Dataset**
[Cat and Dog](https://www.kaggle.com/tongpython/cat-and-dog/kernels)
Consists of ~8k training images and ~2k testing images, divided almost equally between images of cats and dogs.

**Architecture**
- All the models used were pretrained on [ImageNet](http://www.image-net.org/) a dataset of ~14M images having 1000 classes.
- All models except *Inception Resnet V2* were obtained using the [`torchvision.models`](https://pytorch.org/docs/stable/torchvision/models.html) module.
- The *Inception Resnet V2* obtained from [Cadene/pretrained-models.pytorch](https://github.com/Cadene/pretrained-models.pytorch), a nice collection of many pretrained models.
- Pytorch was used for this.
- [COLAB](https://colab.research.google.com/drive/1gMV8g7w3D86ELjb2s0Wfggkl2NwmUH2x)

|Architecture | Params | Inference (CPU) | Inferece (T4) | Accuracy | Loss |
|-----|--------|-----------------|---------------|------|------|
|Resnet50 |23,512,130| 148.1 ms|9.7 ms| 99.38 %|0.32156|
|WideResnet50|22,984,002| 166.8 ms |10.8 ms| 99.38 %|0.32640|
|ResNext50|66,838,338| 324.2 ms|10.3 ms| 99.69 %|0.31897|
|InceptionResnetV2|54,309,538|250.6 ms | 49.2 ms| 98.95 %|0.32489|


---
---

# Week 1 challenges 
## Classification
  **Dataset**
  [Abalone](http://archive.ics.uci.edu/ml/datasets/Abalone) dataset used, target variable is number of rings. Since boundaries between subsequent rings may be too thing the 24 classes have been grouped together to form 6 classes.  

  **Algorithms Used**
  1. Logistic Regression (one vs all)
      - 61.48% (self coded)
      - 68.06% (sklearn)
  2. Naive Bias
      - 51.51%
  3. kNN 
      - 67.22% (self coded)
      - 67.58% (sklearn)
  4. SVM 
      - 69.61% (sklearn)
  5. Decision Trees
      - 60.77% (sklearn)
  6. Boosted Trees
      - 67.10% (sklearn)
  7. Random Forest
      - 67.70% (sklearn)
  8. Neural Networks
      - 68.54% (pytorch)
      - 18.80% (sklearn - overfit)



## Clustering
  **Dataset**
  [Iris](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_iris.html) dataset used, self coded example uses only two features for visualization in 2 dimesions and to show centroid movement paths. Sklearn usage involves all the classes.
  **Accuracy**
  88.33 %

## Linear Regression
  **Dataset**
  [Boston Housing](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_boston.html) dataset used.  
  Self coded implementation uses pytorch to calculate gradients.  
  **MSE/2**
  - Self coded: 205.07
  - Sklearn: 103.55
