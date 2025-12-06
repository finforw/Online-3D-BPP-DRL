# This is a fork of the original work: https://github.com/alexfrom0815/Online-3D-BPP-DRL for academic research purpose.

## Python 3.10 Environment Setup (Compatible with 4090 GPU)
conda create --name my_python310_env python=3.10
pip install -r requirements.txt

## Python 3.7 Environment Setup (deprecated)
conda deactivate
conda remove --name py38_env --all

conda create --name py37_env python=3.7
conda activate py37_env

pip install torch==1.7.0+cu110 -f https://download.pytorch.org/whl/torch_stable.html
pip install numpy==1.17.0 gym==0.14.0 transforms3d==0.4.1 tensorboardX==2.6.2.2 protobuf==3.20.1
conda install numpy==1.17.0
python -c "import torch; print(f'CUDA available: {torch.cuda.is_available()}'); print(f'PyTorch compiled CUDA version: {torch.version.cuda}')"