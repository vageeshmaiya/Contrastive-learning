# Contrastive learning

## Get started
This project has been executed via google colab.

#### Steps To Follow:

1. Download the code from github as a zip file.

2. Extract the contents of the zip file and upload it into google drive.

3. The code to be executed in google colab:  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/13BB40YyJqTADIr1rrp_Xfu4wbX9-2kia)

4. Make sure to set the runtime to GPU before running the code.

5. Make the necessary changes mentioned in the code to get the result.

6. The dataset to be used has to be uploaded in the `datasets/` folder(if not already present).

7. The horizon values can be edited in `datautils.py` script and the number of epochs can be varied in the main code before running it. 

## Usage

To train and evaluate TS2Vec on a dataset the following command is used in the google colab notebook :

```train & evaluate
!python -u train.py <dataset_name> <run_name> --epochs <epochs> --loader <loader> --max-threads <max-threads> --seed <seed> --eval
```
The detailed descriptions about the arguments are as following:
| Parameter name | Description of parameter |
| --- | --- |
| dataset_name | The name of the dataset to be used|
| run_name | The folder name used to save model, output and evaluation metrics. This can be set to any word |
| epochs | The number of epochs the code has to run for (defaults to None) |
| loader | The data loader used to load the experimental data. This can be set to `UCR`, `UEA`, `forecast_csv`, `forecast_csv_univar`, `anomaly`, or `anomaly_coldstart` |
| max-threads | The maximum allowed number of threads used by this process (defaults to None) |
| seed | The random seed (defaults to None) |
| eval | Whether to perform evaluation after training |

After training and evaluation, the trained encoder, output and evaluation metrics can be found in `training/DatasetName__RunName_Date_Time/`


Any other changes such as `batch-size` or `max-train-length` can be done in the `train.py` script.

## Acknowledgement

We appreciate the following github repos a lot for their valuable code base and datasets:

https://github.com/yuezhihan/ts2vec

Diao, W., Saxena, S., Pecht, M. Accelerated Cycle Life Testing and Capacity Degradation Modeling of LiCoO2 -graphite Cells. J. Power
Sources 2019, 435, 226830.

Kollmeyer, Phillip (2018),"Panasonic 18650PF Li-ion Battery Data",
Mendeley Data, V1, doi: 10.17632/wykht8y7tg.1
