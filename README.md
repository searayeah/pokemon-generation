# pokemon-generation

Task: pokemon __image generation__

Dataset: [pokemon-image-dataset](https://www.kaggle.com/datasets/hlrhegemony/pokemon-image-dataset)

Augmentations:

- Resize to 64x64,
- Random horizontal flip
- Color jitter

Training:

- 1000 epochs
- batch_size=128
- Adam: LR = 0.0002 BETA = (0.5, 0.999)

Models:

- DCGAN
- WGAN-GP

Best model: [DCGAN](https://github.com/searayeah/pokemon-generation/blob/main/DCGAN-final.ipynb) with tweaks from [ganhacks](https://github.com/soumith/ganhacks):

- A modified loss function (for G min (log 1-D) --> max log D)
- Label smoothing
- Adding noise to inputs
- LeakyReLU insead of ReLU

Result:
![image](https://user-images.githubusercontent.com/57370975/227232357-c3a40efe-af1f-4aa5-ab9a-e9ad8e215b70.png)
