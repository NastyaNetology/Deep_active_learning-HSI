# Deep_active_learning-HSI

## Setup Instructions

Step 1: Create the Environment

Run the following commands in Anaconda Prompt or Terminal to set up the required environment:
conda create -n multispectral python=3.8
conda activate multispectral
conda install -n multispectral ipykernel --update-deps --force-reinstall
pip install rasterio
pip install geopandas
pip install matplotlib
pip install scikit-learn
pip install tensorflow
pip install fiona==1.9


Step 2: Running the Models
Run the following notebooks in order:
Deep_active_learning.ipynb → Applies deep active learning for more efficient labeling and classification.



## Deep Active Learning in Hyperspectral Image Classification
 
## Introduction to Deep Active Learning
Deep Active Learning (DAL) is an advanced machine learning approach that selects the most 
informative unlabeled samples for annotation, reducing the cost of data labeling while 
improving model performance. Unlike traditional supervised learning, which requires a large fully 
labeled dataset, DAL iteratively queries the most uncertain samples to be labeled by an oracle 
(e.g., human expert).

## Key Idea
The model is initially trained on a small labeled dataset, predicts on unlabeled data, selects the 
most uncertain samples, labels them, and retrains iteratively to improve accuracy.

## Active Learning Process (Used in the Code)

Deep Active Learning consists of the following steps:
1. Train an initial model using a small labeled dataset.
2. Predict on unlabeled data and compute uncertainty scores.
3. Select the most uncertain samples for labeling using query strategies.
4. Retrain the model using both labeled and newly labeled samples.
5. Repeat the process until model performance converges or labeling budget is exhausted.

## Advantages of Deep Active Learning
 Reduces labeling cost by selecting only the most informative samples.
 Improves model performance using fewer labeled data points.
 Efficient in remote sensing where manual annotation is expensive.
 Adapts dynamically as the model learns, reducing redundancy.


## Conclusion
• Deep Active Learning efficiently selects data for annotation, reducing labeling efforts 
while improving accuracy.
• The code implements an uncertainty-based query strategy using entropy sampling.
• This method is highly useful in domains where labeling is expensive, such as remote 
sensing and medical imaging
