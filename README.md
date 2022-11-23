# UW-Madison-GI-Tract-Image-Segmentation
*** Bronze Medal Awarded, Top 10% (149/1548) ***

I want to start this README by thanking my teammates @dssdee @Apolaris and @Jiqing. They were really helpful, and I have learned from them a lot since we have merged. Our final solution was a blend of 2.5D models with psueudo-label. Using imagenet pretraining weight and resnext101 as backbone.

All other approaches we have tried:
CRF, TTA, predicting more slides without labels, mmsegmentation


In this competition we are segmenting organs cells in images. The training annotations are provided as *RLE-encoded masks, and the images are in 16-bit grayscale PNG format*.

Each case in this competition is represented by multiple sets of scan slices (each set is identified by the day the scan took place). Some cases are split by time (early days are in train, later days are in test) while some cases are split by case - the entirety of the case is in train or test. The goal of this competition is to be able to generalize to both partially and wholly unseen cases.
