# vk-try

## Pokemon image generation task

Dataset: https://www.kaggle.com/datasets/hlrhegemony/pokemon-image-dataset

Augmentations: Resize to 64x64, random horizontal flip, color jitter

Trained 1000 epochs batch_size=128 using Adam: LR = 0.0002 BETA = (0.5,0.999)

Models: DCGAN, WGAN-GP

Best model: [DCGAN](https://github.com/searayeah/vk-try/blob/main/DCGAN%20real%20label%20smoothing.ipynb) with tweaks from https://github.com/soumith/ganhacks:
- A modified loss function (for G min (log 1-D) --> max log D)
- Label smoothing
- Adding noise to inputs

Result:
![image](https://user-images.githubusercontent.com/57370975/227232357-c3a40efe-af1f-4aa5-ab9a-e9ad8e215b70.png)

