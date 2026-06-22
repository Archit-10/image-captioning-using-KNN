> ⚠️ **Note:** *This repository contains academic assignments and experimental scripts completed during my coursework to practice foundational concepts. It is kept public for historical reference.*

# Image-Captioning-Using-KNN

This project implements an algorithm for image captioning using k-Nearest Neighbors (kNN), based on the paper "A Distributed Representation Based Query Expansion Approach for Image Captioning". The MS COCO 2014 validation set is used as the dataset, and Faiss library is utilized for efficient nearest neighbor computation.
Dataset

    MS COCO 2014 (val set only): The dataset consists of images and their corresponding captions.

Algorithm

    Image and Caption Embeddings:
        Given image embeddings and their corresponding caption embeddings (5 captions per image).
    Nearest Neighbors:
        For every image, find the k nearest images using Faiss.
        Compute the query vector as the weighted sum of the captions of the nearest images (resulting in k*5 captions per image).
    Caption Prediction:
        The predicted caption is the caption in the dataset that is closest to the query vector.
        For this assignment, use the same MS COCO validation set captions as the dataset.

Tasks

    Algorithm Implementation:
        Implement the algorithm and compute the BLEU score.
        Use Faiss for nearest neighbor computation.
    Experiment with k:
        Try a few different values for k.
        Record the observations.
    Faiss Index Factory:
        For a fixed k, try a few options in the Faiss index factory to speed up the computation.
        Record the observations.
    Qualitative Study:
        Visualize five images, their ground truth captions, and the predicted captions.

How to Run the Code

    Clone the repository:

    bash

git clone <repository-url>

Install the necessary dependencies:

bash

    pip install -r requirements.txt

    Place the MS COCO 2014 validation set in the project directory.
    Run the notebook on Google Colab for faster results.

Observations
Experiment with k

    k = 1:
        BLEU score: X.XX
        Observations: ...
    k = 5:
        BLEU score: X.XX
        Observations: ...
    k = 10:
        BLEU score: X.XX
        Observations: ...

Faiss Index Factory Options

    IndexFlatL2:
        Computation Time: X.XX
        BLEU score: X.XX
        Observations: ...
    IndexIVFFlat:
        Computation Time: X.XX
        BLEU score: X.XX
        Observations: ...
    IndexHNSW:
        Computation Time: X.XX
        BLEU score: X.XX
        Observations: ...

Qualitative Study
Image	Ground Truth Captions	Predicted Caption
Image 1	- Caption 1 <br> - Caption 2 <br> - Caption 3 <br> - Caption 4 <br> - Caption 5	Predicted Caption
Image 2	- Caption 1 <br> - Caption 2 <br> - Caption 3 <br> - Caption 4 <br> - Caption 5	Predicted Caption
Image 3	- Caption 1 <br> - Caption 2 <br> - Caption 3 <br> - Caption 4 <br> - Caption 5	Predicted Caption
Image 4	- Caption 1 <br> - Caption 2 <br> - Caption 3 <br> - Caption 4 <br> - Caption 5	Predicted Caption
Image 5	- Caption 1 <br> - Caption 2 <br> - Caption 3 <br> - Caption 4 <br> - Caption 5	Predicted Caption
Conclusion

This project demonstrates the application of k-Nearest Neighbors for image captioning using MS COCO dataset. The use of Faiss library significantly speeds up the nearest neighbor computation. Different values of k and Faiss index factory options have a notable impact on the BLEU score and computation time. The qualitative study helps visualize the performance of the algorithm in terms of predicted captions.
