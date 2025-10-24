# Installation and specifications

All notebooks use Python 3.11.13

Setup PyTorch with CUDA: <br><br>
Installation Specifications:<br>
Windows 11<br>
RTX 4070 Super<br>
Anaconda Navigator <br>
<br>
Steps:<br>
1 - Create new environment in Anaconda Navigator named torch_env<br>
2 - Select the environment and open terminal<br>
3 - Run: ```conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia```<br>
4 - Run: ```conda install ipykernel jupyterlab```<br>
5 - Run: ```python -m ipykernel install --user --name=torch_env --display-name "PyTorch (CUDA)"```<br>
6 - Launch JupyterLab and change kernel to PyTorch(CUDA)<br>
7 - Run in the first cell of the notebook:<br>
```
import torch
print("PyTorch version:", torch.__version__)
print("CUDA available:", torch.cuda.is_available())
if torch.cuda.is_available():
    print("GPU:", torch.cuda.get_device_name(0))
```
Expected output:
```
PyTorch version: 2.5.1 (basically PyTorch version: 2.x.x)
CUDA available: True
GPU: NVIDIA GeForce RTX 4070 SUPER
```

# CV1.ipynb
The notebook deals with binary image classification (synthetic “surveillance” images): circle (class 0, simulate “person”) vs square (class 1, simulate “vehicle”).

The notebook uses a synthetic shapes dataset.

# CV with LLM.ipynb
Additional dependency:
Sympy version 1.14.0

The notebook builds on the knowledge learned in cv1 and applies a faster R-CNN model trained on a synthetic dataset.

This is also combined with a NLP/LLM setup to output suggested actions/prompts from a list based on the detected entities. 
