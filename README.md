# [Global-Wheat-Detection](https://www.kaggle.com/c/global-wheat-detection)

The challenge in this Kaggle competition is to detect the wheat heads and draw bounding boxes around all the detected wheat heads in the given image. Here are a few example of the predictions generated using FasterRCNN model:


<p float="left">
  <img src="./images/preds1.png" width="250" />
  <img src="./images/preds2.png" width="250" /> 
  <img src="./images/preds3.png" width="250" />
</p>

Here are a few approaches I tried to approach the problem with brief description and achieved score on public leader board (score is mAP (mean average precision) in this competitions).

## Experiment #1 (0.6426 on public LB)
- Used model: COCO Pre-trained FasterRCNN
- No image augmentations
- Other settings:
  - Image size:1024 x 1024
  - No CV
  - 5 Epochs
  - Batch size: 16 images
  
## Experiment #2 (0.6547 on public LB)
- Used model: COCO Pre-trained FasterRCNN
- No image augmentations
- 1 round of training on pseudo Labels
- 5 epochs to train on original data, 4 epochs for training on pseudo labels

 ## Experiment #3 (0.6575 on public LB)
- Used model: COCO Pre-trained FasterRCNN
- No image augmentations
- 2 rounds of training on pseudo Labels
- 5 epochs to train on original data, 4 epochs/round for training on pseudo labels

 ## Experiment #4 (0.6528 on public LB)
- Used model: COCO Pre-trained FasterRCNN
- No image augmentations
- 3 rounds of training on pseudo Labels
- 5 epochs to train on original data, 4 epochs/round for training on pseudo labels

 ## Experiment #5 (0.6498 on public LB)
- Used model: COCO Pre-trained FasterRCNN
- Random Brightness, Contrass, Horizontal and Vertical flips and Hue Saturation Value Image Augmentations
- No pseudo labels
- 12 epochs on augmented dataset: https://www.kaggle.com/kaushal2896/gwdaugmented/version/3

 ## Experiment #6 (0.6826 on public LB)
- Used model: COCO Pre-trained FasterRCNN
- Random Brightness, Contrass, Horizontal and Vertical flips and Hue Saturation Value Image Augmentations
- 2 rounds of psuedo labeling
- 12 epochs on augmented dataset (mentioned on exp #5) and 4 epochs/round for training on pseudo labels

