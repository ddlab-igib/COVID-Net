# Steps to download the COVIDx1k dataset used for testing in CovBaseAI paper

COVIDx1k dataset, used for testing in [CovBaseAI paper](https://www.medrxiv.org/content/10.1101/2020.10.20.20213793v1) and its Ground Truth CSV is available inside the repository at the following location: [Link](../COVIDx1k) 

## COVIDx1k data distribution

Chest radiography images distribution in COVIDx1k
|  Type | Number of images |
|:-----:|:------:|
| Normal | 885 |
|  COVID-19 | 100 |
|  Total | 985 |

# [COVIDx](https://github.com/lindawangg/COVID-Net) Dataset (last updated: 06/26/2020)

<!--We especially thank the Radiological Society of North America, National Institutes of Health, Figure1, Actualmed, M.E.H. Chowdhury et al., Dr. Joseph Paul Cohen and the team at MILA involved in the COVID-19 image data collection project for making data available to the global community.-->

The COVIDx dataset is constructed by the following open source chest radiography datasets:
* https://github.com/ieee8023/covid-chestxray-dataset
* https://github.com/agchung/Figure1-COVID-chestxray-dataset
* https://github.com/agchung/Actualmed-COVID-chestxray-dataset
* https://www.kaggle.com/tawsifurrahman/covid19-radiography-database
* https://www.kaggle.com/c/rsna-pneumonia-detection-challenge (which came from: https://nihcc.app.box.com/v/ChestXray-NIHCC)

 * `git clone https://github.com/ieee8023/covid-chestxray-dataset.git`
 * `git clone https://github.com/agchung/Figure1-COVID-chestxray-dataset.git`
 * `git clone https://github.com/agchung/Actualmed-COVID-chestxray-dataset.git`
 * go to this [link](https://www.kaggle.com/tawsifurrahman/covid19-radiography-database) to download the COVID-19 Radiography database. Only the COVID-19 image folder and metadata file is required. The overlaps between covid-chestxray-dataset are handled
 * go to this [link](https://www.kaggle.com/c/rsna-pneumonia-detection-challenge/data) to download the RSNA pneumonia dataset
2. Create a `data` directory and within the data directory, create a `train` and `test` directory
3. Use [create\_COVIDx.ipynb](https://github.com/ddlab-igib/COVID-Net/blob/master/create_COVIDx.ipynb) to combine the three dataset to create COVIDx. Make sure to remember to change the file paths.
4. We provide the train and test txt files with patientId, image path and label (normal, pneumonia or COVID-19). The description for each file is explained below:
 * [train\_COVIDx2.txt](../train_COVIDx3.txt): This file contains the samples used for training COVIDNet-CXR.
 * [test\_COVIDx2.txt](../test_COVIDx3.txt): This file contains the samples used for testing COVIDNet-CXR.
