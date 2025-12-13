# Computer Vision Image Generation Project

This project contains implementations of DDPM (Denoising Diffusion Probabilistic Models) and VAE (Variational Autoencoder) for generative modeling, along with quantitative  and qualitative analysis.

## Project Report
For a detailed report of this project, please view: [GenCV003_Report.pdf](GenCV003_Report.pdf)

## Repo Files Structure

### DDPM/
Contains DDPM (Denoising Diffusion Probabilistic Model) implementations:

1. **[DDPM/DDPM_Fashion_Mnist.ipynb](DDPM/DDPM_Fashion_Mnist.ipynb)** - Standard DDPM implementation
2. **[DDPM/Conditional_DDPM_Fashion_Mnist.ipynb](DDPM/Conditional_DDPM_Fashion_Mnist.ipynb)** - Conditional DDPM implementation

### VAE/
Contains VAE (Variational Autoencoder) implementations:

1. **[VAE/VAE_Fashion_Mnist.ipynb](VAE/VAE_Fashion_Mnist.ipynb)** - VAE implementation

### Running_Models/
Contains notebooks for running pre-trained models:

1. **Running_Models/DDPM_Running.ipynb** - Run pre-trained DDPM model
2. **Running_Models/VAE_Running.ipynb** - Run pre-trained VAE model

### Quantitative_Analysis/
Contains quantitative analysis and model variants:

- **[Quantitative_Analysis/Quantitaive_Analysis.ipynb](Quantitative_Analysis/Quantitaive_Analysis.ipynb)** - Main quantitative analysis notebook comparing DDPM and VAE generated data

#### Model_variants_for_QA (Model Variants for Quantitative Analysis)
This subfolder contains model variants specifically optimized for quantitative analysis:

1. **Quantitative_Analysis/Model_variants_for_QA/DDPM_T1000_for_QA.ipynb** - DDPM implementation with 1000 timesteps (instead of 4000 steps in the standard implementation) to accelerate image generation needed for metrics computation.

2. **Quantitative_Analysis/Model_variants_for_QA/VAE_for_QA.ipynb** - VAE variant used for image generation during the quantitative analysis phase.

#### Generated Data
The **Quantitative_Analysis/generated_data/** folder contains `.npy` files with saved generated samples from both DDPM and VAE models used for quantitative analysis.

### Saved_DDPM/
The `Saved_DDPM/` folder contains pre-trained Keras model files:

- **diffusion_4000.keras** - Standard DDPM implementation trained with 4000 timesteps.
- **diffusion_1000.keras** - DDPM variant trained with 1000 timesteps, used during the quantitative analysis phase for faster computation.
