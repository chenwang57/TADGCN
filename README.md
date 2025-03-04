# TADGCN: A Time-Aware Dynamic Graph Convolution Network for Long-term Traffic Flow Prediction

This is a TensorFlow implementation of TADGCN.

**Important Notice: Email Update to** chenwang99@buaa.edu.cn

## Requirements

* TensorFlow-gpu==2.5.0
* numpy==1.19.5
* pandas==1.4.1
* networkx==2.6.3
* einops==0.3.2
* gensim==4.1.2
* pyyaml==5.4.1

## Dataset

The datasets used in our paper are collected by the Caltrans Performance Measurement System(PeMS). Please refer to [STSGCN (AAAI 2020)](https://github.com/Davidham3/STSGCN) and [GTA (TITS 2021)](https://github.com/skzhangPKU/GTA) for the download url.

## Run

### Train
***
Before training this model, set `mode: train` in the corresponding yaml file in the `configs` folder, and execute the following command: 

    python main.py --dataset=PEMS04
    or
    python main.py --dataset=PEMS08
    or
    python main.py --dataset=England

### Test
***
Before testing the TADGCN, you should modify `mode: test` and give the best model path. For example:

    best_path: ./experiments/PEMS08/2023-10-06-15-18-30/best_model

Subsequently, execute the following command to test the model:

    python main.py --dataset=PEMS08


## Citation

Please cite the following paper, if you find the repository or the paper useful.

    @article{wang2024tadgcn,
        title={TADGCN: A Time-Aware Dynamic Graph Convolution Network for long-term traffic flow prediction},
        author={Wang, Chen and Zuo, Kaizhong and Zhang, Shaokun and Liu, Chunyang and Peng, Hao and Li, Wenjie and Shen, Zhangyi and Hu, Peng and Wang, Rui and Jie, Biao},
        journal={Expert Systems with Applications},
        pages={125134},
        year={2024},
        publisher={Elsevier}
    }

