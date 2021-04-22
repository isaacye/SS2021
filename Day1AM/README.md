# Day 1 Morning

## What we cover
* Training linear model
* Activation functions
* Loss functions
* Multi-variable linear regression

:pencil2: Lecture slide

### Setting up virtual environment in Graham

Virtual Environment(VE) supported by Python is a working place only for your work, so you can add/delete any packages you need. Here we practice to install necessary packages for ML framework - PyTorch. 

To create a VE on the clusters do the following:
```
module load StdEnv/2020
module load python/3.8.2
module load scipy-stack/2020b
virtualenv --no-download ~/VENV
```
As you may guess, **VENV** is the name of the virtual environment. (You can choose whatever you want)

You can activate your VE by

```
source ~/VENV/bin/activate
```
and deactivate it by typing the command below in the VE

```
deactivate
```

Once it is activated, you can see the command prompt in your terminal changed as follows.

![virtualenv3](https://github.com/isaacye/SS2021/blob/main/Day1AM/ve3.png)

Before installing any packages (modules), you better check if your **pip** (python package manager) is up to date. (Note that it is done once after activating **VE**.)

```
pip install --upgrade pip
```

Now, we need to install PyTorch packages by checking our **wheelhouse**.  
(Note that PyTorch is named as *torch* in our wheelhouse.)

```
avail_wheels torch
```

![virtualenv4](https://github.com/isaacye/SS2021/blob/main/Day1AM/ve4.png)

If you type __avail_whees__, you will have the full list of available wheels in the system. For information on how to search for things like specific versions, see the wiki [here](https://docs.computecanada.ca/wiki/Python#Available_wheels).

To install PyTorch, just type:

```
pip install --no-index torch
```

The portion of this command that specifies the local wheelhouse install is "--no-index". If this is not present, pip will attempt to download the wheel from the internet. 

Once it's successfully installed, you can check by 

```
pip list | grep torch
```


![virtualenv5](https://github.com/isaacye/SS2021/blob/main/Day1AM/ve5.png)

Run Python in the VE to start the interpreter as follows

```python```

and import torch to see if it works fine:

```
import torch
print(torch.__version__)
```

![virtualenv6](https://github.com/isaacye/SS2021/blob/main/Day1AM/ve6.png)


### Running your code in Graham
