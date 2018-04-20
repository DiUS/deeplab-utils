# deeplab-utils
Utilities for working with DeepLab

This is a collection of tools for working with the DeepLab deep learning model, as described in the paper [Rethinking Atrous Convolution for Semantic Image Segmentation](https://arxiv.org/pdf/1706.05587.pdf). We used the model implementation [here](https://github.com/rishizek/tensorflow-deeplab-v3).

In the first instance we needed to create our own masks for training. We used [Labelbox](labelbox.io) for segmenting our images, and exported the project in their JSON format. Within this file there is a reference to a binary mask for each label category. However, the DeepLab implementation assumes the training set to be in Pascal VOC format, which combines the category masks into a combined, single-channel instance mask. Each pixel in the combined mask has a value corresponding to the category number.
