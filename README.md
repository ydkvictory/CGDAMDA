# CGDAMDA
A novel miRNA-disease association prediction model based on an adaptive content-guided fusion mechanism and DilateFormer

MicroRNAs (miRNAs) play a key role in gene expression regulation, and to identify miRNA-disease associations (MDAs) is of great significance for disease diagnosis and treatment. Due to the high cost of traditional experiments, computational models have become an effective alternative method for predicting MDAs. However, existing methods lack flexibility in fusing and processing features and cannot capture long-range dependencies, which limits the accuracy of predictions. To alleviate these problems, we propose a MDAs prediction model based on adaptive content-guided fusion mechanism and DilateFormer, named CGDAMDA. Firstly, the CGDAMDA generates various similarity information for miRNAs and diseases. It adjusts the weights of each similarity matrix using an adaptive content-guided fusion mechanism to automatically focus on the similarity information that contributes to the prediction task. Secondly, sliding window attention and multi-scale dilated attention are used to extract local and global features. Finally, the learned feature representations of miRNAs and diseases are connected and fed into the XGBoost classifier for training and prediction of potential MDAs. In the 5-fold cross-validation experiment, the AUC values of our model on the HMDD V2.0 and HMDD V3.2 datasets are 0.9585±0.0041 and 0.9632±0.0021, respectively, which are better than several state-of-the-art prediction models. Moreover, the case studies about breast cancer and lung cancer further demonstrate the effectiveness of our method.

The flowchart of CGDAMDA.(1) similarity feature information. (2) feature fusion and enhancement. (3) feature encoding via DilateFormer networks. (4) train and prediction of MDAs by XGBoost

## Requirements

CGDAMDA is tested to work under:

python == 3.9

pytorch ==2.1.0+cu118

torch-geometric == 2.5.2

scipy == 1.13

numpy == 1.26.4

sklearn == 1.4.2

pandas == 2.1.4

matplotlib == 3.8.2

## Running the Code

Execute **main_hmdd20.py**  or **main_hmdd32.py** to run the code

## Note

```
Torch-geometric has a strong dependency, so it is recommended to install a matching version.
```
