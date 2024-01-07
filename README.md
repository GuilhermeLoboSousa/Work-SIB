# Sistemas Inteligentes para a Bioinformática

## Drug Synergy Prediction

**Definition**: Synergy is a dimensionless measure of deviation of an observed drug combination response from the expected effect of non-interaction. Synergy can be calculated using different models such as the Bliss model, Highest Single Agent (HSA), Loewe additivity model and Zero Interaction Potency (ZIP). Another relevant metric is CSS which measures the drug combination sensitivity and is derived using relative IC50 values of compounds and the area under their dose-response curves.

**Impact**: Drug combination therapy offers enormous potential for expanding the use of existing drugs and in improving their efficacy. For instance, the simultaneous modulation of multiple targets can address the common mechanisms of drug resistance in the treatment of cancers. However, experimentally exploring the entire space of possible drug combinations is not a feasible task. Computational models that can predict the therapeutic potential of drug combinations can thus be immensely valuable in guiding this exploration.

**Generalization**: It is important for model predictions to be able to adapt to varying underlying biology as captured through different cell lines drawn from multiple tissues of origin. Dosage is also an important factor that can impact model generalizability.

**Product**: Small-molecule.

**Pipeline**: Activity.

Link:https://tdcommons.ai/multi_pred_tasks/drugsyn/

**Dataset Description**: A large-scale oncology screen produced by Merck & Co., where each sample consists of two compounds and a cell line. The dataset covers 583 distinct combinations, each tested against 39 human cancer cell lines derived from 7 different tissue types. Pairwise combinations were constructed from 38 diverse anticancer drugs (14 experimental and 24 approved). The synergy score is calculated by Loewe Additivity values using the batch processing mode of Combenefit. The genomic features are from ArrayExpress database (accession number: E-MTAB-3610) and was quantile normalized and summarized with Factor Analysis for Robust Microarray Summarization (FARMS). The processed data is provided by DeepSynergy.

**Task Description**: Regression. Given the gene expression of cell lines and two SMILES strings of the drug combos, predict the drug synergy level.

**Dataset Statistics**: 23,052 drug combo-cell line points, among 39 cancer cell lines and 37 drugs

This work is divided in 4 main parts:
Parte 1 has an initial exploration of the dataset and respective pre-process, where we standardize data, get descriptors, morgan fingerprinting, check visual chemical structure of the drugs, eliminate NAN values and outliers, do feature selection, and show some visual representation of the data.

In Parte 2, we will explore various unsupervised analysis techniques to gain insights into the relationships between features in our dataset. We will start by examining the correlation between features using a correlation plot. Next, we will employ Principal Component Analysis (PCA) to reduce the data's dimensionality and identify the most important characteristics. Subsequently, we will use t-SNE to visualize high-dimensional data in a two-dimensional space. Finally, the K-Means clustering algorithm will be applied to group similar data points and identify any underlying patterns in the data.

In Parte 3, we compare the performance of various machine learning models on the dataset, analyze the algorithms' behavior by calculating appropriate error metrics, and utilize suitable error estimation methods. Finally, we aim to present the best-performing model.

In Parte 4, we want to explore some Deep Learning models on the dataset.
