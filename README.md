# Comparision between Mini-CovidNet and MobileNetV2

This work is based on the paper: Mini-COVIDNet: Efficient Lightweight Deep Neural Network for Ultrasound Based Point-of-Care Detection of COVID-19 and https://github.com/navchetan-awasthi/Mini-COVIDNet. 

## Dataset

The dataset utilized in this work is available at: https://github.com/jannisborn/covid19_pocus_ultrasound/tree/master/data
Lung ultrasound videos are decoded and frames are extracted out of these videos as part of data pre-pocessing. The videos also have the frames which are not so relevant to the labelled class. For example, A video belonging to a covid patient will have few frames at the start or end of the video which doesn't reflect covid infection in lungs. As part of data- pre-processing these frames are removed from the dataset. Some of the video frames have a depth marker at the right side of the frames. The depth markers were removed from the frames as they have potential to confuse the model. The dataset is split into training ,validation and test set.

### Processed dataset

The preprocessed dataset is available at the link - https://drive.google.com/drive/folders/1Ye7yoVNnBIKhylNVHkDgy7E06cZz8gk0?usp=sharing

## Models used for the comparision

### MobileNetV2

This architecture uses NASNetMobile, a convolutional neural network architecture from the NAS (Neural Architecture Search) family, optimized for mobile and embedded vision applications. It is known for its efficiency in terms of computational cost and model size while maintaining competitive performance. 

### Mini-COVIDNet

This model employs MobileNet as its base. MobileNet architectures are known for their depth-wise separable convolutions which significantly reduce the number of parameters compared to conventional convolutional layers, making them highly efficient for deployment in mobile and edge devices.
