# PhysNet

Tensorflow implementation of PhysNet (see https://arxiv.org/abs/1902.08408) for details

## Requirements

To run this software, you need:

- python3 (tested with version 3.6.3)
- TensorFlow (tested with version 1.10.1)

## Environment
```
conda create -y -n physnet python=3.5
conda activate physnet
conda install -y tensorflow-gpu=1.10.0
conda install -y ipykernel
ipython kernel install --user --name=physnet
#
conda deactivate
conda env list
conda env remove -n physnet
```

## How to use

Edit the config.txt file to specify hyperparameters, dataset location, training/validation set size etc.
(see "train.py" for a list of all options)

Then, simply run

```
# Prepare data
mkdir data && cd data
wget https://zenodo.org/record/2605341/files/sn2_reactions.npz
wget https://zenodo.org/record/2605341/files/README.txt
wget https://zenodo.org/record/2605341/files/read_data.py
cd ..

# Training
python3 train.py 
```

in a terminal to start training. 

The included "config.txt" assumes that the dataset "sn2_reactions.npz" is present. It can be downloaded from: https://zenodo.org/record/2605341. In order to use a different dataset, it needs to be formatted in the same way as this example ("sn2_reactions.npz"). Please refer to the README file of the dataset (available from https://zenodo.org/record/2605341) for details.



