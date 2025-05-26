# GAN-based Handwritten Digit Generator

This project explores Generative Adversarial Networks (GANs) for synthesizing realistic handwritten digit images using the MNIST dataset. We experimented with both fully connected and convolutional GAN architectures, gradually optimizing hyperparameters, loss functions, and training strategies to improve generation quality. The best-performing model (DCGAN-like) was trained for 200 epochs, producing sharp and well-structured digits.

## Contents  

`data/`   
- `dataset.md` - Details on loading the MNIST dataset via torchvision  

`models/`   
- `generator.pt` - Final trained generator model (200 epochs)  
- `generator_weights.pt` - Saved weights for reuse and inference  

`notebooks/`  
- `notebook.md` – Google Colab-ready notebook containing full model training, visualization, and inference logic

## Approach
- Explored 16 different GAN configurations (fully connected + DCGAN variants) with techniques like batch normalization, dropout, and tanh activations. Tuned learning rate, batch size, activation functions (ReLU vs. LeakyReLU), and epochs.
- Best results from DCGAN-based architecture trained for 200 epochs.
- Introduced transposed convolutions to improve image sharpness.

## Key Results  

| Model ID | Epochs | Architecture   | Activation | Notes                                    |
| -------- | ------ | -------------- | ---------- | ---------------------------------------- |
| Model 6  | 60     | FC layers      | ReLU/Tanh  | Clear digits, some noise remains         |
| Model 9  | 100    | FC + LeakyReLU | Tanh       | Best performance (fully connected)       |
| Model 16 | 200    | DCGAN (Conv)   | LeakyReLU  | **Best overall** - sharp, diverse digits |
