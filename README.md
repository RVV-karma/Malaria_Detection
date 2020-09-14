# Malaria_Detection
A deep learning model to classify healthy and malaria infected person from their blood smear images.  
Achieved accuracy is **96.8125 %**


## Models
5 models/techniques are used in this Jupyter Notebook. Their accuracies are as follows:
1. Basic CNN                                                          (without Data Augmentation)  --  95.9525 %
2. Transfer Learning        (VGG-19)                        (without Data Augmentation)  --  93.2750 %
3. Transfer Learning        (fine-tuned VGG-19)      (without Data Augmentation)  --  96.6000 %
4. Transfer Learning        (fine-tuned VGG-19)      (with Data Augmentation)       --  96.7625 %
5. Ensembling (3) and (4)                                                                                        --  96.8125 %

# Conclusions
1.   Shallow network (with just 3 CNN layers) overfits the data very early (in just about 4 epochs), but provides a good accuracy too.
2.   Using deeper architecture results in higher accuracy only when we fine-tune the network by training middle layers too.
3.   On using data augmentation, we get a little higher accuracy. But it is very beneficial as the validation loss is effectively less compared to non-augmented model. So, it predicts with higher confidence.
4.   Ensembling the model makes benefits from both the models. Thus instead of getting the mean accuracy of the two, we get slightly higher accuracy than both the individual models.
