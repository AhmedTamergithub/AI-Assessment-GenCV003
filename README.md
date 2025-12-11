# CV Generation Project

This project contains implementations of DDPM (Denoising Diffusion Probabilistic Models) and VAE (Variational Autoencoder) for generative modeling, along with quantitative  and qualitative analysis.

## Project Report
For a detailed report of this project, please view: [GenCV003_Report.pdf](GenCV003_Report.pdf)

## Running the Models

### 1. DDPM (Denoising Diffusion Probabilistic Model)
To run the standard DDPM implementation, run all cells in  the following notebook from top to down:
- [DDPM/DDPM_Fashion_Mnist.ipynb](DDPM/DDPM_Fashion_Mnist.ipynb)

### 2. Conditional DDPM
To run the conditional DDPM implementation,  run all cells in  the following notebook from top to down:
- [DDPM/Conditional_DDPM_Fashion_Mnist.ipynb](DDPM/Conditional_DDPM_Fashion_Mnist.ipynb)

### 3. Variational Autoencoder (VAE)
To run the VAE implementation, run all cells in this notebook:
- [VAE/VAE_Fashion_Mnist.ipynb](VAE/VAE_Fashion_Mnist.ipynb)
 
## Quantitative Analysis
The [Quantitative_Analysis/Quantitaive_Analysis.ipynb](Quantitative_Analysis/Quantitaive_Analysis.ipynb) notebook contains quantitative analysis and comparison of generated data from both DDPM and VAE models.

### Model Variants for Quantitative Analysis (Model_variants_for_QA)
This subfolder contains model variants specifically optimized for quantitative analysis:

1. **DDPM_T1000_for_QA.ipynb** - DDPM implementation with 1000 timesteps (instead of 4000 steps in the standard implementation) to accelerate image generation needed for metrics computation.

2. **VAE_for_QA.ipynb** - VAE variant used for image generation during the quantitative analysis phase.

3. **generated_data/** - Contains `.npy` files with saved generated samples from both DDPM and VAE models.

## Saved DDPM Models
The `Saved_DDPM/` folder contains pre-trained Keras model files:

- **diffusion_4000.keras** - Standard DDPM implementation trained with 4000 timesteps.
- **diffusion_1000.keras** - DDPM variant trained with 1000 timesteps, used during the quantitative analysis phase for faster computation.
