# MSDS (Gemma Moran)

## Installation
Download Anaconda [here](https://www.anaconda.com/download).
(Note: there are a variety of different python distributions; for statistics and machine learning, we recommend Anaconda.)

### Creating an environment for MSDS-534
We recommend creating a virtual environment for your MSDS-534 coding projects.
1. Open Terminal
2. Create an environment called `msds534` using `conda` with the command:
   ```conda create --name msds534```
3. To install packages in your environment, first activate your environment:
   ```conda activate msds534```
4. Then, install the following packages using the command:
   ```conda install numpy pandas matplotlib seaborn scikit-learn```
5. Install PyTorch by running the appropriate command from [here](https://pytorch.org) (for macOS, the command is: `conda install pytorch::pytorch torchvision torchaudio -c pytorch`
6. To exit your environment:
   ```conda deactivate```

Here is a helpful [cheatsheet](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) for `conda` environment commands.

### Share environment
1. Both pip packages and conda packages
```conda env export > environment.yml```
2. Only include packages you've explicitly asekd for.
```conda env export --from-history >file.yml```

Also, this is not the best example of channel ordering in a YAML. Better practice would be priority of pytorch > conda-forge > defaults. When people want Pytorch, that should be highest priority, and if Conda Forge is at all needed, it should almost always take precedence over defaults. Otherwise, one risks encountering channel mixing issues.

### Create an environment from an .yml file
1. Create an environment from an .yml file:                       
```conda env create -f name.yml```
2. To verify that the new environment was installed correctly:               
```conda env list```              
3. Updating an environment:             
```conda env update --prefix ./env --file environment.yml  --prune```             
4.Cloning an environment:               
```conda create --name new_environment --clone existing_env```       
verify with           
```conda ifo --envs```            


