# vk-try

Pokemon image classification task

Dataset: https://www.kaggle.com/datasets/hlrhegemony/pokemon-image-dataset

Augmentations: Resize to 64x64, random horizontal flip, color jitter

Trained using Adam: LR = 0.0002 BETA = (0.5,0.999)

Models: DCGAN, WGAN-GP
G заместо min (log 1-D) --> max log D
Best model: DCGAN with tweaks from https://github.com/soumith/ganhacks:
- A modified loss function (for G min (log 1-D) --> max log D)
- Label smoothing
- Adding noise to inputs

Result:
