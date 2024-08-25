# Food-Vision-Mini
The model is capable of identifying 101 different types of food in an Image.

The Model Was trained on only 10% of the whole (Food101 dataset)[https://paperswithcode.com/dataset/food-101]. 
The full dataset available to download at http://www.vision.ee.ethz.ch/datasets/food-101/

Even though the model was not trained on the full dataset, it was able to beat the original paper which had an accuracy of 50.76%.
**When using the
discriminative component mining together with multi-class svm classification,
we measure an accuracy of 50.76%, an improvement of 8.13% and 11.88% compared to mlds and ifv, respectively. Also on this dataset, cnn set the state of
the art and rfdc are outperformed by a margin of 5.64%. This is paid by a
considerably longer training time of six days on a nvidia Tesla K20X ''' (See the paper)[https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/static/bossard_eccv14_food-101.pdf]**

### Training.
The first part of training involved using EfficientNetV2B2 as the model's backbone to perform Feature extraction. The model achieved a low accuracy of 48% which was lower than the paper.


