# Federated Transfer Learning-based Intrusion Detection System in 5G networks

This project focuses on the development of an Intrusion Detection System (IDS) within 5G, and more specifically IoT networks. The main idea is to implement a Federated Learning (FL) framework that allows to train a global detection model without the need to share data between all devices. The UNSW-NB15 dataset is used for training purposes, using subsets as local datasets. 
However, to improve the detection of unknown attacks, Federated Transfer Learning (FTL) is also implemented, so as to observe the performance improvement. To develop the pre-trained model for FTL, subsets of the Bot-IoT dataset are used. 


## Code Usage and Structure

To obtain the code, it is possible to download the `.zip` file containing all the files in the repository. 

The file structure is the following: 

```
.
├── README.md
├── datasets
│   ├── BOT-UNIFORM
│   │   ├── bot_part1.csv
│   │   ├── bot_part2.csv
│   │   ├── bot_part3.csv
│   │   ├── bot_part4.csv
│   │   └── bot_part5.csv
│   ├── DET-IMBALANCED1
│   │   ├── imb1_part1.csv
│   │   ├── imb1_part2.csv
│   │   ├── imb1_part3.csv
│   │   ├── imb1_part4.csv
│   │   └── imb1_part5.csv
│   ├── DET-IMBALANCED2
│   │   ├── imb2_part1.csv
│   │   ├── imb2_part2.csv
│   │   ├── imb2_part3.csv
│   │   ├── imb2_part4.csv
│   │   └── imb2_part5.csv
│   ├── DET-IMBALANCED3
│   │   ├── imb3_part1.csv
│   │   ├── imb3_part2.csv
│   │   ├── imb3_part3.csv
│   │   ├── imb3_part4.csv
│   │   └── imb3_part5.csv
│   ├── DET-UNIFORM
│   │   ├── uniform_part1.csv
│   │   ├── uniform_part2.csv
│   │   ├── uniform_part3.csv
│   │   ├── uniform_part4.csv
│   │   └── uniform_part5.csv
│   └── TESTS
│       ├── BOT_TEST.csv
│       └── DET_TEST.csv
├── models
│   ├── fedavg
│   │   ├── w_avg_imb1_5_1.hdf5
│   │   ├── w_avg_imb2_5_1.hdf5
│   │   ├── w_avg_imb3_5_1.hdf5
│   │   └── w_avg_unif_5_1.hdf5
│   ├── geomed
│   │   ├── Local and Global DET-IMBALANCED1 models
│   │   │   ├── desktop.ini
│   │   │   ├── node0w_geo_imb1_5_1.keras
│   │   │   ├── node1w_geo_imb1_5_1.keras
│   │   │   ├── node2w_geo_imb1_5_1.keras
│   │   │   ├── node3w_geo_imb1_5_1.keras
│   │   │   ├── node4w_geo_imb1_5_1.keras
│   │   │   └── w_geo_imb1_5_1.hdf5
│   │   ├── Local and Global DET-IMBALANCED2 models
│   │   │   ├── desktop.ini
│   │   │   ├── node0w_geo_imb2_5_1.keras
│   │   │   ├── node1w_geo_imb2_5_1.keras
│   │   │   ├── node2w_geo_imb2_5_1.keras
│   │   │   ├── node3w_geo_imb2_5_1.keras
│   │   │   ├── node4w_geo_imb2_5_1.keras
│   │   │   └── w_geo_imb2_5_1.hdf5
│   │   ├── Local and Global DET-IMBALANCED3 models
│   │   │   ├── FL
│   │   │   └── FTL
│   │   ├── Local and Global DET-UNIFORM models
│   │   │   ├── desktop.ini
│   │   │   ├── node0w_geo_unif_5_1.keras
│   │   │   ├── node1w_geo_unif_5_1.keras
│   │   │   ├── node2w_geo_unif_5_1.keras
│   │   │   ├── node3w_geo_unif_5_1.keras
│   │   │   ├── node4w_geo_unif_5_1.keras
│   │   │   └── w_geo_unif_5_1.hdf5
│   │   └── Pre-trained Global model - Bot-IoT
│   │       └── w_bot_5_5.hdf5
│   ├── krum
│   │   ├── w_kr_imb1_5_1.hdf5
│   │   ├── w_kr_imb2_5_1.hdf5
│   │   ├── w_kr_imb3_5_1.hdf5
│   │   └── w_kr_unif_5_1.hdf5
│   └── median
│       ├── w_med_imb1_5_1.hdf5
│       ├── w_med_imb2_5_1.hdf5
│       ├── w_med_imb3_5_1.hdf5
│       └── w_med_unif_5_1.hdf5
├── notebooks
│   ├── FL_w.ipynb
│   ├── FTL.ipynb
│   ├── creation_det_test.ipynb
│   ├── evaluation.ipynb
│   ├── partitions_bot.ipynb
│   └── partitions_det.ipynb
└── requirements.txt
```

There are three different folders in the repository to be taken into account. The first one is `datasets`, 
which contains the different dataset partitions for training purposes and the test datasets. 

Then, there is the `models` folder, which contains the different evaluated models, divided based on the aggregation function used, and the dataset partitions used. 

Finally, the `notebooks` folder contains all the code that has been used to create all datasets, train the models, and evaluate them. Each file has the following content: 

    * FL_W.ipynb: File for training FL models. Includes functions for each aggregation function. 
    * FTL.ipynb: File for training FTL models. 
    * creation_det_test.ipynb: Generation of the DET_TEST dataset. 
    * evaluation.ipynb: Evaluation code to determine evaluation metrics of certain model. 
    * partitions_bot.ipynb: Creation of the Bot-IoT dataset partitions. 
    * partitions_det.ipynb: Creation of the UNSW-NB15 dataset partitions. 


## References 

This project has been based by ``

The Github repository for the code is: https://github.com/polvalls9/Transfer-Learning-Based-Intrusion-Detection-in-5G-and-IoT-Networks.git 
