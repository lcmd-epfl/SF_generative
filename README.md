# SF_generative

This repository contains the scripts, configuration files, and software components used for training generative models and performing reinforcement learning. It includes pre-RL and post-RL generative models, as well as the Chemprop model for excited-state property prediction.

## Repository Structure

- `configs/`: Configuration files for various stages of the project.
- `data/`: Data files used in the project.
- `model/`: Model checkpoints and related files.
- `script/`: Scripts for various tasks.

<!-- <!-- ## Usage -->


1. **Setup the Environment**: Use the `environment.yml` file to set up the required conda environment.
   ```sh
   conda env create -f environment.yml
   conda activate sf_generative
   ``` 

   If you have the model trained with REINVENT v.3, use  `convert_r3_model.py` to make it compatible with REINVENT v.4.
    
    To make singlet fission score component visible to REINVENT v.4,
    `bash
    export PYTHONPATH="${PYTHONPATH}:[]/SF_generative/script"
    `

2. **Run REINVENT task**: Use TOML files in  `configs/` directory to optimize the generative model in  `model/` for singlet fission chromophores

   ```sh
   reinvent rl.toml -l rl.log  
   ``` 
    
    
     

3. **Post-optimization analysis**: Use python scipts in `scipts/` directory to visualize the optimization history, analzye the optimized generative model, 
and sample for singlet fission candidates

   ```sh
   python rl_analysis.log
   python model_analysis.log

   ``` 


## Citation

If you use this repository in your research, please cite the following publication:


```
Worakul T, Laplaza R, Blaskovits JT, Corminboeuf C. Generative Design of Singlet Fission Materials by Revisiting the Use of a Fragment-oriented Database. ChemRxiv. 2025; doi:10.26434/chemrxiv-2025-chmsm
```


