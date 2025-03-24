
1. Make conda environment
```
conda create -n pytorch18 python=3.8
conda activate pytorch18
```

1. Install dependencies
```
git clone https://github.com/gladzhang/Xformer.git
cd Xformer
pip install torch==1.8.0+cu111 torchvision==0.9.0+cu111 torchaudio==0.8.0 -f https://download.pytorch.org/whl/torch_stable.html
pip install -r requirements.txt
```

1. Install basicsr
```
python setup.py develop --no_cuda_ext
```

2. Download pretrained weights from [This Google Drive](https://drive.google.com/drive/folders/1XTz_xwm6u9ZSbUcRFq8ObSPSalp2GAkT?usp=sharing) and place under 'model_zoo' folder. 
3. to run the test code: 
```
python evaluate/test_gaussian_color_denoising.py --sigma 50
```

