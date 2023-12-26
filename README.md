# Foundation Model for Quantitative Imaging Analysis in Breast Cancer 

<p align="center">
  <img src="https://user-images.githubusercontent.com/17007301/219617294-a5f38b07-4599-4834-aa7c-96d01299a531.png" width="600" height="300">
</p>


## Welcome to Foundation Model for Breast Cancer MRI (FM-BCMRI).

FM-BCMRI is a vertical foundation model for quantitative MRI analysis in breast cancer. FM-BCMRI is trained on a diverse dataset covering various breast cancer types and stages, and it undergoes meticulous data preprocessing, ensuring optimal input quality. Harnessing advanced deep learning techniques (contrastive learning algorithms), the model extracts deep learning-based features from MRI scans, unveiling crucial insights into contrast enhancement patterns, shape characteristics, and texture features. Positioned for versatile applications in both research and clinical realms, it empowers researchers with nuanced data exploration and provides healthcare professionals with support for informed decision-making.

The FM-BCMRI is designed and developed by Dr.Zhenwei Shi, Zhihe Zhao, Zhitao Wei, Dr.Chu Han and other AI/CS scientists from [Media Lab](https://github.com/GDPHMediaLab). Also, the work is supported and guided by experienced radiologists Prof. MD Zaiyi Liu and Prof. MD Changhong Liang from the radiolgoy department of Guangdong Provincial People's Hospital.

## Major Features

<p align="center">
<img width="594" alt="FM-BCMRI-figure" src="https://github.com/zhenweishi/FM-BCMRI/assets/17007301/77fe4202-5dde-4c4e-ac59-27c6254873c2">
</p>

The FM-BCMRI model was pre-trained by using constrative learning algorithms (Figure A). The FM-BCMRI can be implemented to specific use cases by extracting quantitative imaging features or by task-specitic fine-tuning (Figure B). 
## Installation

```
pip install foundation-model-bcmri
```


## Quick Start

For easy use, we provide an example notebook to introduce the functionalities of our package. 

### Step 1. Package Loading


```
import fmbcmri
``` 


### Step 2. Parameter Setting and input file preparison

The package has a defalt parameter setting file, which including image processing parameters. Users can modify them according to their own studies. Also, for the processing, the users are required to prepare an input csv file, see below. The csv file has two columns including the image and ROI mask pathes. 

```sh
from fmbcmri import preprocessing

local_path = r'/workingdir/'
input_file = preprocessing.inputgenerate(local_path)
```

### Step 3. Feature extraction

According to input image and region of interest region (ROI) mask, the FM-BCMRI can extract quantitative deep learnig-based features. The features are saved in an output csv file. 


```sh
from fmbcmri import get_features

df_feature = get_features("input_csv")
df_feature.to_csv('output_features.csv',index = None)
```

### Step 4. Quantitative analysis of the extracted features

To understand and explain the extracted feautures well, the FM-BCMRI package provides a fine workflow for feature analysis and visualization.

```sh
from fmbcmri import feature_analysis
import pandas as pd

df_feature = pd.read_csv('output_features.csv')
df_feature = get_features("input_csv")
feature_analysis(df_feature)
```
The above codes will generate several results and figures, such as feature dimension reduction, feature inter-correlation and so on.

### Step 5. Machine learning-based modelling by AutoML

We also integrate auto-machine learning algorithms in the FM-BCMRI package, which can use the extracted features for downstream leison segmentaton, classification and regression tasks.

```sh
from fmbcmri import automl

model = automl("input_csv")
model.summary()
```


## License

This project is freely available to browse, download, and use for scientific and educational purposes as outlined in the [Creative Commons Attribution 3.0 Unported License](https://creativecommons.org/licenses/by/3.0/).

## Disclaimer

FM-BCMRI is still under development. Although we have tested and evaluated the workflow under many different situations, it may have errors and bugs unfortunately. Please use it cautiously. If you find any, please contact us and we would fix them ASAP.

## Main Developers
 - [Dr. Zhenwei Shi](https://github.com/zhenweishi) <sup/>1, 2
 - MSc. Zhihe Zhao <sup/>2, 3
 - MSc. Zhitao Wei <sup/>2, 4
 - MSc. Xiaodong Zheng <sup/>2, 4
 - [Dr. Chu Han](https://chuhan89.com) <sup/>1, 2
 - MD. Changhong Liang <sup/>1, 2
 - MD. Zaiyi Liu <sup/>1, 2
 

<sup>1</sup> Department of Radiology, Guangdong Provincial People's Hospital (Guangdong Academy of Medical Sciences), Southern Medical University, China <br/>
<sup>2</sup> Guangdong Provincial Key Laboratory of Artificial Intelligence in Medical Image Analysis and Application, China <br/>
<sup>3</sup> School of Medicine, South China University of Technology, China <br/>
<sup>4</sup> Institute of Computing Science and Technology, Guangzhou University, China <br/>
<sup>5</sup> Department of Medical Imaging, Nanfang Hospital, Southern Medical University, China 

## Contact
We are happy to help you with any questions. Please contact Dr Zhenwei Shi.

We welcome contributions to FM-BCMRI.
