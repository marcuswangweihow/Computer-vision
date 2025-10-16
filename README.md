# Computer-vision

Setup PyTorch with CUDA: <br><br>
Device Requirements:<br>
Windows 11<br>
RTX 4070 Super<br>
Anaconda Navigator <br>
<br>
Steps:<br>
1 - Create new environment in Anaconda Navigator named torch_env<br>
2 - Select the environment and open terminal<br>
3 - Run: conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia<br>
4 - Run: conda install ipykernel jupyterlab<br>
5 - Run: python -m ipykernel install --user --name=torch_env --display-name "PyTorch (CUDA)"<br>
6 - Launch JupyterLab and change kernel to PyTorch(CUDA)<br>
7 - Run in the first cell of the notebook:<br>
import torch<br>
print("PyTorch version:", torch.__version__)<br>
print("CUDA available:", torch.cuda.is_available())<br>
if torch.cuda.is_available():<br>
&emsp;&emsp;print("GPU:", torch.cuda.get_device_name(0))<br>
<br>
Expected output:<br>
PyTorch version: 2.5.1 (basically PyTorch version: 2.x.x)<br>
CUDA available: True<br>
GPU: NVIDIA GeForce RTX 4070 SUPER<br>
