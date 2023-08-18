# Music-genre-classification-with-different-CNNs
Using different CNN models to train on GTZAN Dataset
You can download the whole dataset from: https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification

Results up to now:
1. GoogleNet : Test Accuracy: Around 55% - 60%
   
3. Newly Designed CNN: Test Accuracy(10 genres): Around 70% - 80%            Test Accuracy(5 genres): Around 85%
   
   Architecture:
   
   MelSpecClassifier(
  (b1): Sequential(
    (0): Conv2d(1, 64, kernel_size=(7, 7), stride=(2, 2), padding=(3, 3))
    (1): ReLU()
    (2): MaxPool2d(kernel_size=3, stride=2, padding=1, dilation=1, ceil_mode=False)

  )
  (conv2): Conv2d(64, 256, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
  
  (relu2): PReLU(num_parameters=1)
  
  (bn2): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
  
  (conv3): Conv2d(256, 512, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
  
  (relu3): PReLU(num_parameters=1)
  
  (bn3): BatchNorm2d(512, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
  
  (conv4): Conv2d(512, 256, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
  
  (relu4): PReLU(num_parameters=1)
  
  (bn4): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
  
  (conv5): Conv2d(256, 128, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
  
  (relu5): PReLU(num_parameters=1)
  
  (bn5): BatchNorm2d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
  
  (drp): Dropout2d(p=0.4, inplace=False)
  
  (ap): AdaptiveAvgPool2d(output_size=1)
  
  (fc): Linear(in_features=128, out_features=64, bias=True)
  
  (fitter): Sequential(
  
    (0): Sequential(
      (0): Conv2d(1, 64, kernel_size=(7, 7), stride=(2, 2), padding=(3, 3))
      (1): ReLU()
      (2): MaxPool2d(kernel_size=3, stride=2, padding=1, dilation=1, ceil_mode=False)
    )
    
    (1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1))
    
    (2): ReLU()
    
    (3): Conv2d(64, 256, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
    
    (4): PReLU(num_parameters=1)
    
    (5): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
    
    (6): Conv2d(256, 512, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
    
    (7): PReLU(num_parameters=1)
    
    (8): BatchNorm2d(512, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
    
    (9): Conv2d(512, 256, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
    
    (10): PReLU(num_parameters=1)
    
    (11): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
    
    (12): Conv2d(256, 128, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
    
    (13): PReLU(num_parameters=1)
    
    (14): BatchNorm2d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
    
    (15): Dropout2d(p=0.4, inplace=False)
    
    (16): AdaptiveAvgPool2d(output_size=1)
    
    (17): Flatten(start_dim=1, end_dim=-1)
    
    (18): Linear(in_features=128, out_features=64, bias=True)
    
    
    (19): Linear(in_features=64, out_features=10, bias=True)
  )
)

Still trying to explore new CNNs...

Let's test on a Reggae Song:

<img width="752" alt="96_degrees" src="https://github.com/KobeWang-supreme/Music-genre-classification-with-different-CNNswith-different-CNN/assets/78716482/b9b995df-d11c-4735-8da7-55c1bcc5a33f">

Result:

![result](https://github.com/KobeWang-supreme/Music-genre-classification-with-different-CNNswith-different-CNN/assets/78716482/124f157c-52c1-4a21-98d3-9604116a8389)





