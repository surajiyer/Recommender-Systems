# Recommender systems, 2017-18

This repository contains notebooks and other files associated with my class on *Recommender systems* from Eindhoven University of Technology.

- Section 1: Learning CBoW and Skipgram models (with and without negative sampling) to generate words embeddings. Applied to analogy detection and sentence reconstruction.

- Section 2: Learning about neural codes (link to paper: https://arxiv.org/pdf/1404.1777.pdf) to generate image embeddings with and without PCA compression. Three different ways to generate neural codes: Convolutional networks, Denoising Autoencoders, Sparse Autoencoders. Applied to image retrieval with Nearest neighbor detection using neural codes as feature space.

- Section 3: 
  - Learning about Siamese networks & one-shot learning. Training a siamese network on 80 classes from Cifar-100 dataset, then use neural codes to perform multiple N-way one-shot learning tasks on remaining 20 classes. Model performs better than random guessing.
  - Learning about LSTM, GRU, and Bidirectional variants. Applied in generating document sequence embeddings based on binary sentiment classification task. Also used generated embeddings to one-shot learning task on Amazon product reviews dataset.
  - Combining the knowledge of Siamese networks and RNNs to Image-Caption retrieval problem. Preprocessed the data to create triplet instances [<image, positive caption, negative caption>, ...]. Designed a NN architecture that generates image and caption neural codes, combines them, and optimizes a max-margin loss function to increase the bounds between the positive pair embedding and negative pair embedding. Laslty, we use the *kNN* algorithm to recommend top-k nearest images given a caption or top-k nearest captions given an image.
