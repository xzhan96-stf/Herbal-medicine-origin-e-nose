# Herbal medicine origin classification dataset

### `herbal medicine` `open-domain dataset` `geographical origin classification` `electronic nose` 
---


Here we provide our dataset in classifying herbal medicine origins by temporal and spectral data mining of electronic nose.
* [Dataset background](#Dataset_background)
* [Dataset introduction](#Dataset_introduction)

### Dataset_background
Our dataset includes 3 categories of herbal medicine, each with 4 different geographical origins:  

|Category|Chinese name|Origin1|Origin2|Origin3|Origin4|
|---|---|---|---|---|---|
|`Radix Angelicae`|白芷|Anhui|Sichuan|Hubei|Zhejiang|
| `Angelica Sinensis`|当归|Shaanxi|Gansu|Hubei|Sichuan|
| `Radix Puerariae`|葛根|Sichuan|Hubei|Anhui|Hunan|  

- The electronic nose(e-nose) we used was the one in the Biochemistry Microsensing Lab of State Key Laboratory of Industrial Control Technology, Institute of Cyber-Systems and Control, Zhejiang University.  
- This e-nose has 16 TGS types metal oxide semi-conductive sensors that are sensitive to different types of gases. When we pumped in the volatile organic gas of each hermal medicine samples, the e-nose recorded the response signal of each sensors, which  was presented by vlotage changes.  
- The sampling rate was 100HZ and the recording period was in 340s.  
- More details can be access through our previous publications:
[Origin discrimination](https://ieeexplore.ieee.org/abstract/document/8854643/);  [Category discrimination](https://www.mdpi.com/1424-8220/18/9/2936)


### Dataset_introduction
After data pre-processing like baseline value and invalid period removal etc., the temporal data of each sample was in the shape of (1,16,31800). Our feature extraction methods were based on this primitive dataset.
- `Dataset with primitive signal`:The file named with 'BZ_sampling_points.npy','DG_sampling_points.npy','DG_sampling_points.npy' respectively represents the primitive sampling dataset of Radix Angelicae, Angelica Sinensis,Radix Puerariae.  
Each file contains the dataset of 160 samples in the shape of (1,16,31800). The dataset is stacked with origin sequence; For example, the dataset insists of origins A,B,C,D is stacked in the order of 40A-40B-40C-40D.
- `Dataset with extracted features`:The file named with 'BZ_dataset_public.mat','DG_dataset_public.mat', and 'GG_dataset_public.mat'  respectively represents the feature extracted dataset of Radix Angelicae, Angelica Sinensis,Radix Puerariae.  
