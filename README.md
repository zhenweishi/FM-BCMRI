# Foundation Model for Quantitative Imaging Analysis in Breast Cancer 

<p align="center">
  <img src="https://github.com/zhenweishi/FM-BCMRI/assets/17007301/205440be-21a3-48f2-95d2-359ab3d37067" width="1000" height="250">
</p>


## Welcome to Foundation Model for Breast Cancer MRI (FM-BCMRI).

FM-BCMRI is a vertical foundation model for quantitative MRI analysis in breast cancer. FM-BCMRI is trained on a diverse dataset covering various breast cancer types and stages, and it undergoes meticulous data preprocessing, ensuring optimal input quality. Harnessing advanced deep learning techniques (i.e., contrastive learning algorithms), the model extracts deep learning-based features from MRI scans, unveiling crucial insights into contrast enhancement patterns, shape characteristics, and texture features. Positioned for versatile applications in both research and clinical realms, it empowers researchers with nuanced data exploration and provides healthcare professionals with support for informed decision-making.

The FM-BCMRI is designed and developed by Dr.Zhenwei Shi, Zhihe Zhao, Zhitao Wei, Dr.Chu Han and other AI/CS scientists from [Media Lab](https://github.com/GDPHMediaLab). Also, the work is supported and guided by experienced radiologists Prof. MD Zaiyi Liu and Prof. MD Changhong Liang from the radiolgoy department of Guangdong Provincial People's Hospital.

## Major Features

<p align="center">
<img src="https://github.com/zhenweishi/FM-BCMRI/assets/17007301/77fe4202-5dde-4c4e-ac59-27c6254873c2" width="1000" height="450">
</p>

The FM-BCMRI model was pre-trained by using constrative learning algorithms (Figure A). The FM-BCMRI can be implemented to specific use cases by extracting quantitative imaging features or by task-specitic fine-tuning (Figure B). 
## Installation

Before using the FM-BCMRI foundation model, we suggest users create a vistual environment. Some example codes are as follows:
```
conda create --name fmbcmri python==3.8
conda activate fmbcmri
```
Then install related dependencies.

```
pip install -r requirements.txt
```
If the installation runs slowly, you can try the following method

```
pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
```

## Quick Start (10 mins)

The FM-BCMRI model can be used in two manners (Figure B). For easy use, we provide an example notebook to describe how it works. The example codes are in Jupyter notebooks.
Note that, users should download the FMBCMRI model from the [link](https://drive.google.com/drive/folders/1hQiwAwHooyc83x7eCl8PKtYfL-MWH5yd?usp=drive_link) firstly. Also, users need to download test data from the [link](https://drive.google.com/drive/folders/1KDfO58b_41GwCADvjcwQ-RLwpvwVNyai?usp=drive_link) .
```
[main_directory]/notebooks/[pretrained_checkpoint]
[main_directory]/notebooks/[dataset]
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

## Contact
We are happy to help you with any questions. Please contact Dr Zhenwei Shi.

We welcome contributions to FM-BCMRI.
