# Music-genre-classification-with-different-CNNs
Using different CNN models to train on GTZAN Dataset
You can download the whole dataset from: https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification

Results up to now:
1. GoogleNet : Test Accuracy: Around 55% - 60%
   
3. Newly Designed CNN:
   
                        With only Mel n_feature = 128:  Test Accuracy(10 genres): Around 70% - 80%    (baseline: 10%)        Test Accuracy(5 genres): Around 85%   (baseline: 20%)


                        With Mfcc n_feature = 128:     Test Accuracy(10 genres): Around 82%, which is almostly equal to the accuracy with both Mel and Mfcc
   

                        With Mel and Mfcc(added together) n_feature = 128:    Test Accuracy(10 genres): Around 83%     (baseline: 10%)    Test Accuracy(5 genres): Around 91% !!!!  (baseline: 20%)




   
   


Confusion Matrics:


<img width="500" alt="1" src="https://github.com/KobeWang-supreme/Music-genre-classification-with-different-CNNs/assets/78716482/7543597a-6296-46c7-b123-36bc8179cbc5">




Still trying to explore new CNNs...

Let's test on a Reggae Song:

<img width="752" alt="96_degrees" src="https://github.com/KobeWang-supreme/Music-genre-classification-with-different-CNNswith-different-CNN/assets/78716482/b9b995df-d11c-4735-8da7-55c1bcc5a33f">

Result:

![result](https://github.com/KobeWang-supreme/Music-genre-classification-with-different-CNNswith-different-CNN/assets/78716482/124f157c-52c1-4a21-98d3-9604116a8389)




Findings:
1. Actually, some musics belongs to not only one genre. Such as songs from Norah Jones, many songs of her belongs to both jazz and blues. Our model can only return one genre(with highest score). However, it is also clear that by visualizing scores for every genre, we can see jazz and blues have much higher scores than other genres.

      <img width="259" alt="3" src="https://github.com/KobeWang-supreme/Music-genre-classification-with-different-CNNs/assets/78716482/0d748f10-e239-46f0-851a-217e4f6100dd">

   
Let's take "Don't know why" as an example:


<img width="539" alt="2" src="https://github.com/KobeWang-supreme/Music-genre-classification-with-different-CNNs/assets/78716482/63d1f7f6-a557-48b3-9457-db118814f99c">






