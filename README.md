# Structured Matrix Multiplication



## Data
The data for the *Burgers* and *Shear Layer* experiment can be downloaded from the python files available in `_Data/Burgers` and `_Data/Humidity`. The data for the *Humidity* experiment may be downloaded from the shell script in `_Data/Humidity`, this requires a NASA EarthData account to download. Further instructions for getting started with NASA EarthData are available at this link: [https://www.earthdata.nasa.gov/](https://www.earthdata.nasa.gov/). The data for the *Airfoil* and *Elasticity* experiments are provided by [Li et al., *Fourier Neural Operator with Learned Deformations for PDEs on General Topologies*](https://arxiv.org/abs/2207.05209) and are available in this [Google Drive](https://drive.google.com/drive/folders/1YBuaoTdOSr_qzaow-G-iwvbUI7fiUzu8).


## Training

We formatted the models to be run easily from the `train.py` script. Select the model you wish to run (options `fno`, `ffno`, `ufno`, `geo_fno`, `geo_ffno`, `geo_ufno`, `fno_smm`, `ffno_smm`, `ufno_smm`) and the according experiments (options `Burgers`, `Elasticity`). Some experiments will require certain models to be used, for example, point-cloud data such as airfoil or elasticity require `geo_fno` or one of its variants as opposed to `fno`. 

The best hyperparameters are chosen by default, when the configs in `train.py` are left empty. These are defined in the separate model architectures of each experiment. You can choose to overwrite these by adding corresponding entries in the configs.


The code for the spherical shallow water equations are based on a different setup, which can be run directly from the files (`fno.py`,`sfno.py`,`fno_smm.py`,`fno_smm.py`)


## Hyperparameter Sweep

Running `hyperparameter_sweep.py` with your desired parameters in the configs will grid search for the best architecture.


