## A-Self-supervised-Transformer-Approach-for-Fetal-Heart-Rate-Inpainting-and-Forecasting

This repository is the official Pytorch implementation for AI-powered inpainting and forecasting for fetal heart rate signals: (Arxiv link here)

## Description

Fetal heart rate (FHR) monitoring is crucial for evaluating fetal well-being during prenatal care. Recent advances in monitoring technologies, such as wearable FHR monitors, now allow for easy fetal movement analysis in resource-constrained environments without compromising maternal mobility. However, sensor displacement during free movement or changes in fetal and maternal position often results in signal dropouts, creating gaps in the obtained FHR data. These missing signals impede the extraction of meaningful insights and hinder automated downstream analysis. In this paper, we propose a novel approach using masked transformer-based autoencoders to learn signal reconstruction by focusing on both spatial and frequency components of the data. Our proposed method demonstrates robustness in handling diverse durations of missing data, contributing significantly to the field by performing accurate imputations to complete missing data and forecasting FHR signals. The developed models can be integrated into wearable FHR monitoring devices, creating a robust tool for handling missing samples and improving data integrity. This enhancement enables more reliable downstream analysis, potentially leading to earlier detection of fetal distress.

![image](https://github.com/user-attachments/assets/1570e5fe-4147-4006-91fa-7275228d2e41)


# Requirements
- Histolab
- Pytorch
- Pandas
- Numpy
- Scikit-learn
- MMCV
- Scipy

Use requirement.txt for exact versions. 

### Usage:
1. main.py is the script for training transformer-based autoencoders using different parametric settings. 
2. myfunction.py has all the helper functions to run the following files. 

The following files can be used to run forecasting and painting applications. Weights of trained models are required. 
3. TimeGPT-forecasting.py - demo of using TimeGPT model for baseline. API from TimeGPT is required to run forecasting. 
4. interpolation_app.py - shows AI-powered interpolation/inpainting, requires path to trained model weights.
5. forecasting_app.py - performs forecasting using the trained models. 

The following files are just for visualiation or simpler processing.
6. plotting_signals.py - uses preprocessed (.mat) files for plotting.  
7. plot_new_interpolated_dataset.py - plot the new version of the dataset (.npz) files to show some examples.
8. inpainting_data_v3.py - example of inpainting points over the preprocessed signal. 
9. create_interpolation_histogram.py - plots the percentage of interpolation across the data to understand how much data was missing from the original FHRs.



### Results
![image](https://github.com/user-attachments/assets/c474fdda-7e96-453d-940e-8156cd2a7191)


Model weights:
Model weights used in the paper are available at: https://drive.google.com/drive/folders/1zYHzgeG6IsYNvQW-QHVdnj--9oet4gWi?usp=sharing
or using the following links.
1. https://ux.uis.no/self-supervised_model1.dat
2. https://ux.uis.no/self-supervised_model2.dat

## Citing
If you use or find this code repository useful, consider citing it as follows:
```@misc{}}

```





