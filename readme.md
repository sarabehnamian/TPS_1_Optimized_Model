## Temporal Population Structure (TPS.1) - Optimized Model

This repository contains the code and datasets for our recent optimization of the Temporal Population Structure (TPS) model, a genomic dating machine learning-based method for ancient genomes.

## About
The TPS model was initially introduced in our paper "Temporal Population Structure: A Genetic Dating Method for Ancient Eurasian Genomes from the Past 10,000 Years" (Behnamian et al., 2022). In the optimization of the Temporal Population Structure (TPS) model, we adapted our approach to prevent randomness and ensure fair comparisons, focusing specifically on our dataset and the coding process.
We augmented our dataset by incorporating N = 29 Viking genomes. The DateBP of these genomes showed a lower spread in their standard deviations (SD(SD) = 17) in comparison to the Reich dataset (SD(SD) = 34), yet they presented a higher maximum standard deviation (MaxSD = 125) than the Reich dataset (MaxSD = 87). These new Viking samples were included in the training set, while the test set remained unchanged from the original TPS model. In our code, we refined the cross-validation process. Rather than shuffling the data in each round of cross-validation, we shuffled it a single time prior to the onset of cross-validation. This method guaranteed the same order of data in each run, enhancing the consistency and reproducibility of the cross-validation splits. To avoid random selection, we also chose the model with the smallest median absolute error (MedAE) from cross-validation.
The inclusion of a relatively small number of samples, 29 Viking genomes, did not significantly alter the overall accuracy as expected. Differences between the reported and predicted DateBP values for the test set were as follows before and after the inclusion of Viking genomes: (mean = 489, SD = 651, Max = 4640) and (mean = 494, SD = 657, Max = 4565), respectively. Considering the 58 Viking genomes in the test set, it was expected that including 29 additional Viking genomes in the training set could subtly improve the accuracy of Viking predictions. This assumption was affirmed by the resulting data (median with Vikings = 142, without Vikings = 144; Max with Vikings = 2338, without Vikings = 2719).

## Data
The dataset used in this project comprises 3,591 ancient and 1,307 modern Eurasians, along with 29 new Viking genomes added in this optimization process. The data can be found in the /data directory of this repository.

## Getting Started
1.	Clone this repository to your local machine.
2.	Make sure you have all the necessary packages installed. You can find them in TPS.1.ipynb.
3.	Follow the steps listed below to run the pipeline on your dataset.

## Steps 
• STEP0 - Convert genotype file: Description

•	STEP1 - Merge your file with the temporal components: Description

•	STEP2 - Calculate the temporal components of your samples: Description

•	STEP3 - Predict 'merge.8.Q' data file: Description

For a more detailed explanation of each step and the code involved, please refer to the [TPS repository](https://github.com/sarabehnamian/Origins-of-Ancient-Eurasian-Genomes)
.

## The Code
The Jupyter notebook TPS.1.ipynb contains our code and explanations. The notebook is organized into the following sections:
1.	Data Access
2.	Data Exploration
3.	Data Preparation
4.	Model Training
5.	Model Use (Prediction)
6.	Model Evaluation
The explanations in the notebook will guide you through these steps in detail.

## Contributing
We welcome contributions from the community. If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are warmly welcome.

## Contact
For any queries or discussions related to this project, feel free to reach out to sara.behnamian@biol.lu.se

## Citation
If you find our work helpful or use our code or data in your research, please consider citing our original paper:
Behnamian, S., Esposito, U., Holland, G., Alshehab, G., Dobre, A.M., Pirooznia, M., Brimacombe, C.S., & Elhaik, E. (2022). Temporal Population Structure: A Genetic Dating Method for Ancient Eurasian Genomes from the Past 10,000 Years. [DOI: 10.1016/j.crmeth.2022.100270]
 [Behnamian, S., Esposito, U., Holland, G., Alshehab, G., Dobre, A.M., Pirooznia, M., Brimacombe, C.S., & Elhaik, E. (2022). Temporal Population Structure: A Genetic Dating Method for Ancient Eurasian Genomes from the Past 10,000 Years. [DOI: 10.1016/j.crmeth.2022.100270]](https://www.sciencedirect.com/science/article/pii/S2667237522001473?via%3Dihub)



