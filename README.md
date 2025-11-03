# waveform-prediction
Waveform Estimation in Piezoelectric Inkjet Printing Utilizing Multi-Material Inks

# Conda Environment Setup Guide
This guide provides instructions for installing Conda, creating a Conda environment, and installing the required dependencies using the provided `environment.yml` file, and running the deep learning (DL) and machine learning (ML) models.

# Instructions to Install Conda and Set Up the Environment
Step 1. Install Conda:
   - Download the installer for Miniconda or Anaconda:
     - Miniconda: https://docs.conda.io/en/latest/miniconda.html
     - Anaconda: https://www.anaconda.com/products/distribution
   - Run the installer and follow the setup instructions for your operating system.
   - Verify the installation:
     conda --version

Step 2. Open an Anaconda Prompt terminal.

Step 3. Navigate to the directory where `environment_CPU.yml` is saved:
   cd /path/to/directory

Step 4. Create the Conda environment:
   - For the CPU environment:
     conda env create -f environment_CPU.yml
   - For the GPU environment:
     conda env create -f environment_GPU.yml

Step 5. Verify the environment is created:
   conda env list

Step 6. Activate the environment:
   - For the CPU environment:
     conda activate tensor
   - For the GPU environment:
     conda activate tensorGPU

Step 7. Verify that the required libraries are installed:
   conda list
   pip list

Notes:
   - Replace `/path/to/directory` with the actual path where the `.yml` files are located.
   - If you encounter issues with pip packages, ensure pip is installed and updated:
     conda install pip
     pip install --upgrade pip
   - The GPU libraries are configured for Nvidia GTX 1650. For other GPUs, refer to the TensorFlow compatibility guide to adjust the library versions: https://www.tensorflow.org/install/source
   - Experimental dataset used in this article is available online at https://www.eecs.yorku.ca/~grau/MLIJ/Supplementary%20material.zip.

# File Descriptions:
   Following files can be run using Jupyter-lab under the Anaconda environment as described in above section.
   - data_split.ipynb
     This file helps to concatenate individual dataset files to a single file, and then splitting that file into train and test datasets.
   - DL_model_train_test.ipynb
     The data pre-processing can be performed on the dataset, and then DL model can be trained and evaluated on preprocessed data file using this script.
   - GSCV_ML_model_train_test.ipynb
     The data pre-processing can be performed on the dataset, and then a GridSearch operation be performed on the ML models to find the best optimal hyperparameters of each model.
   - ML_model_train_test.ipynb
     The data pre-processing can be performed on the dataset, and then ML models can be trained and evaluated on a preprocessed data file using this script.
