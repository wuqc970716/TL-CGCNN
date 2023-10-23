Transfer learning based on CGCNN

This code is a modification to Crystal Graph Convolutional Neural Networks, or CGCNN proposed by Tian Xie and J. C. Grossman [T. Xie and J. C. Grossman, Crystal graph convolutionalneural networks for an accurate and interpretable prediction of material properties, Physical Review Letters 120,145301 (2018).]

This code allow you to fix the embedding layer, all the convolutional layers and the first following full-connected layer of the CGCNN learnt from a large dataset, and add additional full-connected layers following transferred layers to account for the difference between the large and the small datasets.

Compared with other existing TL models based on CGCNN, this one allows multiple full-connected layers to be added rather than only allowing one additional layer to be added. It can be used to transfer trained CGCNN model with more than 1 full-connected layers.

This code should be put in the same path as the original CGCNN. Make sure that the environment required for CGCNN is set, and the source model is already obtained. Both pth.tar and .pth documents of the source model should be reserved.

For training: python TL-CGCNN.py source.pth.tar sample

For predicting: python tl_predict.py model.pth sample
