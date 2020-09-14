# Brain-tumour-detection-segmentation-and-localization-from-brain-MRI-scans
In this project I have developed total two models. First one is made by Residual Network to classify brain MRI scan images having tumour or not. Here I haven’t built the ResNet by myself, instead of that I have used ‘transfer learning’ and used already trained ResNet by downloading. But on top of ResNet I have added other fully connected layers and that layers I trained by myself. Basically this model will use an image classification technique and predict whether an image has tumour or not. Now coming to the next and final model which localizes the tumour in an image, predicted as having a tumour. In this second model I have use ResUNet which performs much better for segmentation and localization problems. Here I have developed the whole model. For the first model I have got almost 92% of validation accuracy and for the second one I have got almost 99% of validation accuracy. 

I have got the dataset from kaggle:
link: https://www.kaggle.com/mateuszbuda/lgg-mri-segmentation

We need a custom loss function to train this ResUNet. So, we have used the loss function as it is from: 
https://github.com/nabsabraham/focal-tversky-unet/blob/master/losses.py
