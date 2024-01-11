# Cancer Subtype Classification

Final Project for
Applied Machine Learning in Genomic Data Science

## Participants
- Bao Tran Nguyen
- Ben Flügge
- Hauke Schüle
- Meike Liedtke
- Tatjana Wehrmann

## Intro
We used the TCGA Kidney Cancers Dataset that contains transcriptome profiles of patients diagnosed with three
different subtypes of kidney cancers. The dataset is used to make predictions about the specific subtype of kidney cancer.
In the datasets patients with kidney chromophobe cancer are underrepresentated with only 8,85% of the total dataset. Samples of the kidney renal clear cell carcinoma represent the majority of the dataset with 59,73% and the remaining 31,42% are of the kidney renal papillary carcinoma cancer type.
After preprocessing the data, we performed a PCA. We performed the classification on the original and the PCA data both with a decision tree and a feed-forward neural network.

## content

- **1_Data_preprocessing.ipynb**  
**needs:** data/ folder with three subfolders containing raw patient data  
**produces:** original_tpm_data.csv  
creates a csv of the tpm data used for model training

- **2_PCR.ipynb**  
**needs:** original_tpm_data.csv  
**produces:** pca_data_080.csv or pca_data_100.csv  
creates two different datasets treated with pca for feature reduction

- **3_DecisionTree.ipynb**  
**needs:** original_tpm_data.csv, pca_data_080.csv or pca_data_100.csv    
**produces:** None  
creates different decision trees using one of the three datasets. prints model outputs of each version and test statistics over 10 seeded random runs.

- **4_NeuralNetwork.ipynb**  
**needs:** original_tpm_data.csv, pca_data_080.csv or pca_data_100.csv    
**produces:** None  
creates a Neural network using one of the three datasets. Prints test outputs and statistics over 10 seeded random runs.

## usage

Of the three used datasets used, 2 are included in the repository. The dataset "Orignal Data" is not included in git, because of its size restrictions. You can download it [here](https://1drv.ms/u/s!ArCCSMcsPLPhyUX-HYHqGYIx8Q6Z?e=8eLGO0) or run the first notebook, which uses the raw data files in the data folder.

When executing the second notebook PCA, you need the orignial dataset "original_tpm_data.csv".Depending on the execuded code cells, it will produce pca dataset with approx. 80% or 100% explained variance respectively.

When running Notebooks 3 and 4 with the machine learning models, one of the three data-csvs is needed. Most of the experiments mentioned in the report are conducted using the original data.