## FHRFormer: A Self-supervised Transformer Approach for Fetal Heart Rate Inpainting and Forecasting

This repository is the official Pytorch implementation for AI-powered inpainting and forecasting for fetal heart rate signals: https://arxiv.org/abs/2509.20852

## Description

Approximately 10\% of newborns require assistance to initiate breathing at birth, and around 5\% need ventilation support. Fetal heart rate (FHR) monitoring plays a crucial role in assessing fetal well-being during prenatal care, enabling the detection of abnormal patterns and supporting timely obstetric interventions to mitigate fetal risks during labor. Applying artificial intelligence (AI) methods to analyze large datasets of continuous FHR monitoring episodes with diverse outcomes may offer novel insights into predicting the risk of needing breathing assistance or interventions. Recent advances in wearable FHR monitors have enabled continuous fetal monitoring without compromising maternal mobility. However, sensor displacement during maternal movement, as well as changes in fetal or maternal position, often lead to signal dropouts, resulting in gaps in the recorded FHR data. Such missing data limits the extraction of meaningful insights and complicates automated (AI-based) analysis. Traditional approaches to handling missing data, such as simple interpolation techniques, often fail to preserve the spectral characteristics of the signals. In this paper, we propose a masked transformer-based autoencoder approach to reconstruct missing FHR signals by capturing both spatial and frequency components of the data. The proposed method demonstrates robustness across varying durations of missing data and can be used for signal inpainting and forecasting. The proposed approach can be applied retrospectively to research datasets to support the development of AI-based risk algorithms. In the future, the proposed method could be integrated into wearable FHR monitoring devices to achieve earlier and more robust risk detection.

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
### Proposed Model
<img width="827" height="732" alt="image" src="https://github.com/user-attachments/assets/39c5c45b-7615-473b-bce8-f64bb77c8a77" />

### Usage:
1. main.py is the script for training transformer-based autoencoders using different parametric settings. 
2. myfunction.py has all the helper functions to run the following files. 

The following files can be used to run forecasting and painting applications. Weights of trained models are required. 
3. TimeGPT-forecasting.py - demo of using the TimeGPT model for baseline. API from TimeGPT is required to run forecasting. 
4. interpolation_app.py - shows AI-powered interpolation/inpainting, requires path to trained model weights.
5. forecasting_app.py - performs forecasting using the trained models. 

The following files are just for visualization or simpler processing.
6. plotting_signals.py - uses preprocessed (.mat) files for plotting.  
7. plot_new_interpolated_dataset.py - plot the new version of the dataset (.npz) files to show some examples.
8. inpainting_data_v3.py - example of inpainting points over the preprocessed signal. 
9. create_interpolation_histogram.py - plots the percentage of interpolation across the data to understand how much data was missing from the original FHRs.



### Results
![image](https://github.com/user-attachments/assets/c474fdda-7e96-453d-940e-8156cd2a7191)


#### Inpainting Performance
<img width="1029" height="810" alt="image" src="https://github.com/user-attachments/assets/02dbb0ea-bf4e-4c48-ad66-c5d964df0f01" />

#### Forecasting Performance
<img width="1001" height="605" alt="image" src="https://github.com/user-attachments/assets/71706006-f887-4870-8b77-b35c5b5e2b2f" />



Model weights:
Model weights used in the paper are available at: https://drive.google.com/drive/folders/1zYHzgeG6IsYNvQW-QHVdnj--9oet4gWi?usp=sharing
or using the following links.
1. https://ux.uis.no/self-supervised_model1.dat
2. https://ux.uis.no/self-supervised_model2.dat

## Citing
If you use or find this code repository useful, consider citing it as follows:
```
@article{engan2025fhrformer,
  title={FHRFormer: A Self-supervised Transformer Approach for Fetal Heart Rate Inpainting and Forecasting},
  author={Engan, Kjersti and Kanwal, Neel and Yeconia, Anita and Blacy, Ladislaus and Munyaw, Yuda and Mduma, Estomih and Ersdal, Hege},
  journal={arXiv preprint arXiv:2509.20852},
  year={2025}
}

```





