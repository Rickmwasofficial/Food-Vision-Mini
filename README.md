# Food-Vision-Mini
The model is capable of identifying 101 different types of food in an Image.

The Model Was trained on only 10% of the whole [Food101 dataset](https://paperswithcode.com/dataset/food-101). 
The full dataset available to download at http://www.vision.ee.ethz.ch/datasets/food-101/

Even though the model was not trained on the full dataset, it was able to beat the original paper which had an accuracy of 50.76% by getting an accuracy of 53.55%
**When using the
discriminative component mining together with multi-class svm classification,
we measure an accuracy of 50.76%, an improvement of 8.13% and 11.88% compared to mlds and ifv, respectively. Also on this dataset, cnn set the state of
the art and rfdc are outperformed by a margin of 5.64%. This is paid by a
considerably longer training time of six days on a nvidia Tesla K20X ''' (See the paper)[https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/static/bossard_eccv14_food-101.pdf]**

### Training.
The first part of training involved using EfficientNetV2B2 as the model's backbone to perform Feature extraction. The model achieved a low accuracy of 48% which was lower than the paper.

## Loss Curves
![Training Loss Curves](https://github.com/user-attachments/assets/0f1d836a-0eae-4a99-8ec4-d145507a3528)

## Accuracy Curves
![Accuracy Curves](https://github.com/user-attachments/assets/413d26bf-6862-4d31-b8ba-25ac331bf247)

The second part involved fine tuning the feature extraction model, by unfreezing the final 10 layers of the backbone, and reducing the learning rate for the Adam optimizer to 0.0001. The loss curves obtained show that is the model is trained for longer, it would provide even better results before it starts overfitting.

## Loss curves
![Loss Curves of the fine tuned Model](https://github.com/user-attachments/assets/9b030861-5a97-447f-9e0d-c19f4ac298d8)


## Accuracy Curves
![Accuracy curves of the fine tuned model](https://github.com/user-attachments/assets/67aeef28-1a69-43b4-8b9d-c6fb82e4158d)

# Making Predictions

![image](https://github.com/user-attachments/assets/0f919d62-6ec3-42e3-b233-b7a68965d16a)
![image](https://github.com/user-attachments/assets/01cc2410-cf27-43a6-8f3c-826633bc049e)

