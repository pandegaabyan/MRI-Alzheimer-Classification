# Multi-Class Alzheimer's Classification on Brain MRI Data Using DenseNet169, ResNet50, and VGG16 Models

Various studies have utilized deep learning for Alzheimer's classification. This study focuses on four-class classification of Alzheimer's. Three models were tested and compared: DenseNet169, ResNet50, and VGG16. Testing showed that all three models performed well in terms of accuracy and AUC, with accuracies of 97.16%, 94.67%, and 98.89% respectively. Overall, the VGG16 model demonstrated superior performance from various aspects. However, compared to the other two models, the training time for VGG16 was three times longer, which should be considered.

---

The dataset is obtained from [kaggle](https://www.kaggle.com/tourist55/alzheimers-dataset-4-class-of-images) and consists of **MRI data** with four classes of Alzheimer **(MildDemented, ModerateDemented, NonDemented, VeryMildDemented)**. 

The dataset is **large but severely unbalanced**. Therefore, augmentation is necessary, especially for classes with limited data. The data has already been split into "train" and "test" sets, but the distribution was uneven. Hence, it was further divided into three sets ("train", "val", "test") using random sampling to achieve better uniformity.

Testing was conducted using **DenseNet169, ResNet50, and VGG16 models** to compare their performance. For each model, additional parameters and layers were adjusted to optimize performance specific to that model.

Key metrics evaluated in this study include **loss value, accuracy, precision, recall, and AUC**. Plots were also generated to visualize the trends of these metrics across epochs.

Various references were consulted for this study, with the primary source being the [code](https://www.kaggle.com/brycesmith/smith-burns-cosmas-99-testaccuracy/comments) by **Bryce Smith and colleagues**.
