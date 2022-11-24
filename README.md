# UW-Madison-GI-Tract-Image-Segmentation
*** Bronze Medal Awarded, Top 10% (149/1548) ***

I want to start this README by thanking my teammates @dssdee @Apolaris and @Jiqing. They were really helpful, and I have learned from them a lot since we have merged. Our final solution was a blend of 2.5D models with psueudo-label {25D_pseudolabel.py}. Using imagenet pretraining weight and resnext101 as backbone. 

All other approaches we have tried:
CRF{25D_crf.py}, TTA{25D_tta_ensenble.py}, predicting more slides without labels{Predict_more.py}, mmsegmentation{reference 1}

Potential reasons for other approaches above does not better than our final solution:
1. CRF: grayscale MRI images were used
2. Predicting more slides without labels: test set also have images without labels
3. TTA: organs have relative positions, and vertical/horizontal flips may induce bias?
4. mmsegmentation: it is a great approach, but we do not have enough time to refine this approach 


References:
1. MMsegmentation end-to-end notebook  https://www.kaggle.com/competitions/uw-madison-gi-tract-image-segmentation/discussion/323921
2. Pseudo-label https://www.youtube.com/watch?v=SsnWM1xWDu4
3. UWMGI: 2.5D stride=2 Data; https://www.kaggle.com/code/awsaf49/uwmgi
4. UWMGI: 2.5D [Train] [PyTorch] https://www.kaggle.com/code/awsaf49/uwmgi
5. UWMGI: 2.5D [Infer] [PyTorch] https://www.kaggle.com/code/awsaf49/uwmgi
