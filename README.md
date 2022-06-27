# Monodepth2

논문: Monodepth2

Eval.AI : [Monocular Depth Estimation(Self-supervised)](http://203.250.148.128:3088/web/challenges/challenge-page/47/overview)

베이스라인 코드: https://github.com/y2sman/2022.ComputerVision.Final

설명 영상: https://youtu.be/5NSL32r4u0I


## ⚙️ Setup

```
Docker 이미지 : 10.0-cudnn7-devel-ubuntu18.04
Torch 버전 : pytorch=0.4.1 torchvision=0.2.1
GPU : 2080TI
```

## Training

```shell
OMP_NUM_THREADS=1 CUDA_VISIBLE_DEVICES=5 python train.py --model_name kjlee_mono --png --log_dir /home/kjlee/workspace/computervision/Sejong_computervision_termproject_monodepth/logs
```

### Pretraining

```shell
OMP_NUM_THREADS=1 CUDA_VISIBLE_DEVICES=5 python train.py --model_name finetuned_mono --load_weights_folder /home/kjlee/workspace/computervision/Sejong_computervision_termproject_monodepth/models/weights_19
```
