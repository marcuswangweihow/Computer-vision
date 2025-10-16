# Computer-vision

Setup PyTorch with CUDA: 
Device Requirements:
Windows 11
RTX 4070 Super
Anaconda Navigator 

Steps:
1 - Create new environment in Anaconda Navigator named torch_env
2 - Select the environment and open terminal
3 - Run: conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia
4 - Run: conda install ipykernel jupyterlab
5 - Run: python -m ipykernel install --user --name=torch_env --display-name "PyTorch (CUDA)"
6 - Launch JupyterLab and change kernel to PyTorch(CUDA)
7 - Run in the first cell of the notebook:
import torch
print("PyTorch version:", torch.__version__)
print("CUDA available:", torch.cuda.is_available())
if torch.cuda.is_available():
    print("GPU:", torch.cuda.get_device_name(0))

Expected output:
PyTorch version: 2.5.1 (basically PyTorch version: 2.x.x)
CUDA available: True
GPU: NVIDIA GeForce RTX 4070 SUPER
