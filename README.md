# Table of Contents

| Section | Description |
|---------|-------------|
| [Introduction](#introduction) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[Materials](#materials) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[Methods](#methods) |  |
| [Data Exploration](#data-exploration) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[SmartSeq](#smartseq) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[MCF 7](#mcf-7) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[HCC 1806](#hcc-1806) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[DropSeq](#dropseq) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[MCF 7](#mcf-7) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[HCC 1806](#hcc-1806) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Reading the dataset and showing the first 5 rows](#reading-the-dataset-and-showing-the-first-5-rows) |  |
| [Data Preprocessing](#data-preprocessing) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[SmartSeq](#smartseq) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[SmartSeq MCF7 Unfiltered](#smartseq-mcf7-unfiltered) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Quality Control](#quality-control) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Normalization and Transformation](#normalization-and-transformation) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Identifying High Variable Genes](#identifying-high-variable-genes) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[SmartSeq HCC1806 Unfiltered](#smartseq-hcc1806-unfiltered) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Quality Control](#quality-control) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Normalization and Transformation](#normalization-and-transformation) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Identifying High Variable Genes](#identifying-high-variable-genes) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[DropSeq](#dropseq) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[DropSeq MCF7 Filtered](#dropseq-mcf7-filtered) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[DropSeq HCC1806 Filtered](#dropseq-hcc1806-filtered) |  |
| [Unsupervised Learning](#unsupervised-learning) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[DropSeq](#dropseq) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[MCF7](#mcf7) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[PCA](#pca) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Clustering](#clustering) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[HCC1806](#hcc1806) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[PCA](#pca) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Clustering](#clustering) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[SmartSeq](#smartseq) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[MCF7](#mcf7) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[PCA](#pca) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Clustering](#clustering) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[HCC1806](#hcc1806) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[PCA](#pca) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Clustering](#clustering) |  |
| [Supervised Learning](#supervised-learning) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[Dropseq](#dropseq) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[MCF7](#mcf7) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Logistic Regression (97% ACCURACY)](#logistic-regression-97-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[K-Nearest Neighbors (94.5% ACCURACY)](#k-nearest-neighbors-94-5-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Support Vector Machine and Kernel SVM (97% ACCURACY)](#support-vector-machine-and-kernel-svm-97-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Kernel Support Vector Machine (97.5% ACCURACY)](#kernel-support-vector-machine-97-5-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Naive Bayes (82% ACCURACY)](#naive-bayes-82-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Random Forest (94.6% ACCURACY)](#random-forest-94-6-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[HCC1806](#hcc1806) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Logistic Regression (94.5% ACCURACY)](#logistic-regression-94-5-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[K-Nearest Neighbors (92% ACCURACY)](#k-nearest-neighbors-92-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Support Vector Machine (94.5% ACCURACY)](#support-vector-machine-94-5-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Kernel Support Vector Machine (95.5% ACCURACY)](#kernel-support-vector-machine-95-5-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Naive Bayes (93.5% ACCURACY)](#naive-bayes-93-5-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Random Forest (94% ACCURACY)](#random-forest-94-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[SmartSeq](#smartseq) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[MCF7](#mcf7) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Logistic Regression (100% ACCURACY)](#logistic-regression-100-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Support Vector Machine and Kernel SVM (100% ACCURACY)](#support-vector-machine-and-kernel-svm-100-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Kernel Support Vector Machine (100% ACCURACY)](#kernel-support-vector-machine-100-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Naive Bayes (92% ACCURACY)](#naive-bayes-92-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Random Forest (99% ACCURACY)](#random-forest-99-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[HCC1806](#hcc1806) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Logistic Regression (97.9% ACCURACY)](#logistic-regression-97-9-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[K-Nearest Neighbors (95% ACCURACY)](#k-nearest-neighbors-95-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Support Vector Machine (98.6% ACCURACY)](#support-vector-machine-98-6-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Kernel Support Vector Machine (97.2% ACCURACY)](#kernel-support-vector-machine-97-2-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Naive Bayes (93% ACCURACY)](#naive-bayes-93-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Random Forest (97.2% ACCURACY)](#random-forest-97-2-accuracy) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[Supervised Learning Conslusion](#supervised-learning-conslusion) |  |
| [Predictions](#predictions) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[SmartSeq](#smartseq) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[MCF7](#mcf7) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[HCC1806](#hcc1806) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;[DropSeq](#dropseq) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[MCF7](#mcf7) |  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[HCC1806](#hcc1806) |  |
| [Conclusion](#conclusion) |  |

# Introduction

## Materials

In this project, we are given the opportunity to look at four different bilological datasets, each made up of two different types of cells and each using two different RNA sequencing methods. The features (or more specifically the genes) of our dataset are expressed as rows, while our sample cells are expressed as columns. Importantly, each cell has a label that represents whether it has been kept in a hypoxic or a normoxic environment. Our main goal is to produce a model for each database such that it learns to predict the correct labels given the gene expression of the cell. More specifically regarding our case studies: HCC1806 is an epithelial cell line isolated from the mammary gland of a 60-year-old, Black, female patient with acantholytic squamous cell carcinoma (ASCC), while MCF-7 is a breast cancer cell line isolated from a 69-year-old woman. The two sequencing methods employed are SmartSeq and DropSeq with the former resulting in deeper sequencing but also not suitable for a large amount of samples while the latter, despite its more shallow sequencing, works better on a larger number of cells. Therefore, to summarize, the DropSeq databases have more samples but less intrinsic information for each cell, while the SmartSeq databses have less samples but a fuller RNA sequence per samples. We will begin, quite standardly, with data exploration to get a better idea of the data we are dealing with, preprocessing it so we are certain it is ready for training, then proceeding with unsupervised and then supervised learning, picking the best model for each dataset, and finally making our final predictions on the test set, thus concluding our results.

## Methods

Throughout this project we will employ various methods, both pertaining to supervised and unsupervised learning. Our general goal is to be able to distinguish between hypoxic and normal cells, using the examples described above, in the Materials section. To that end, we will approach various concepts and models we tackled in our classes, such as PCA for visualization. We will perform clustering using KNN and various hierarchical algorithms, hoping to get a better idea of the data at hand. While we were also given filtered and normalized datasets, a specific part of our research focused on data pre-processing, since we wanted to also develop personal approaches and skills related to dealing with raw, unfiltered data. While it was not our initial goal by any means, we also learned various tools and parameters to be dealing with bioinformatics, especially by discovering new sources such as Bioconductor.org, a website that helped us with various recommendations on thresholds to deal with pure genomic data. However, the key part of our research is realized in the supervised learning part, where we will be comparing how various models such as: Random Forests, Support Vector Machine, Logistic Regression, K Nearest Neighbors and Naive Bayes will behave on our data and choose the best one to use on the test set and predict the final values.

# Data Exploration

## SmartSeq

#### MCF 7

As mentioned above, the first steps are quite standard. We first look at the meta data. It is a great start for getting familiar with the dataset. It tells us important details about the structure that will be key later on in our research. In our case most of the metadata is simply put a breakdown of the column names of the SmartSeq MCF7 database (where each one represents a different cell) with some aditional information that may not be included in the name. In the metadata, each row represents a different cell while each column corresponds with a different feature that tells us for instance the condition of the cell, its position etc.

Next we look at the actual dataset. In this part we will explore without making any actual changes to the data. This is a crucial step to help us understand what we are dealing with and to help us figure out the necessary steps to take in the preprocessing phase and as a whole in the project. By printing the first 10 rows we see that each column is a different cell, as mentioned above, while each row represents a different gene. The numerical value for each gene in a given cell is the gene expression level or simply how much of that gene is in the cell. It is important to note that, only from such a small section of our database, we already see intriguing details. First, the dataset seems to be quite sparse with a lot of 0s (i.e. a lot of unexpressed genes). Another thing that comes to our attention is the fact that some genes have expression levels that are on average higher than other genes. This might pose some issues in certain approaches like PCA so a normalization might be required.

Two peculiar things also are that our samples are the columns while the futures are rows. Of course there is nothing wrong with that but should be kept in mind in order to prevent any confusion or issues with methods that expect the "standard" orientation. Similarly, we see that we have a much higher feature count than the sample size so dimensionality reduction would most likely benefit our database in order to be able to train a model more effectively.

Next we proceed by looking at the columns. We confirm that each column represents a different cell with some information presented in the name. We also look at the indices, which again show us that each row is a different gene.

We continue by looking at the details of the databse. We observe that different cells and different genes have quite different means of expression and standard deviations. This would suggest that normalization, standardization and log transform on the data could make models perform better.

In this next step, we check if all of our datatypes are numeric. In our case they are but if they were not we would have had to take extra steps in order to get our data ready for analysys, pca, and further training.

Next, we check for missing values. If such exist we may need to drop either the gene or the sample or use some other mothod to deal with the null. Thankfully in this case there are no missing values.

Below, we check for outliers in both the features and the samples. In the features case we plot the variance of the genes and see a great spike at around 0 and a long tail to the right. This confirms that our data is sparse and that many genes are for "housekeeping" and don't change a lot, which in general is to be expected when dealing with RNA, but the long tail to the right suggests that few genes have extreamly high variance. It could either be noise or carry significant information. We also plot the same thing on the log scale to gain more clarity on the distribution. Likely the low variable genes can be safely discarded as they would not provide any significant insight and dependency and we can essentialy keep the "outliers" (i.e the genes with higher variance) as they could be crucial for our classification problem later on.

When plotting the total reads we see that the majority is clustered around 1 million with a few outliers around 2 million. They are likely still valid just with deeper sequenccing. On the left side however we see a big spike around 0. These are the cells that have less than 100 000 reads and hence likely low quallity. We will deal with them in the preprocessing. Additionally, we also plot the mitochondrial percentage of cells and the numbers of expressed genes. These three plots will give us a good idea of important distributions, helping us figure out the cutoffs for certain samples that may be of low qallity. In the threee cases we see some tails that we could cut off in order to remove outliers and cells that are of low quallity.

We can further check if our data is normalised with a simple plot. We select only some of the samples but that will be enough to show us that our data is not normalised. This is something we might want to change as even if two cells express the same genes at the same true biological level, one might appear to have more expression simply because it was sequenced more deeply. Without normalization, you'd mistake technical differences for biological ones.

Also we check that the genes are not normalized and since they are our features, genes that naturally have higher expression values might dominate certain algorithms and prevent us from discovering dependencies on less expressed features.

We can also look for ourliers through the IQR. This gives us the spread of expression values within each cell. The issue is that the dataset is quite sparse so the genes that actually carry information for the cells are the ones that have values different from 0, but since many of the genes have a value 0, the "flagged" outliers are actually the genes with higher values (i.e exactly the information carrying geneses). We will bump into the same issue in the case of the Smartseq HCC1806 database below.

#### HCC 1806

We continue our exploration with the SmartSeq HCC1806 dataset.

We can again start with the meta data. There is no need for further explanation as the sequencing method is the same as the MCF7 case discussed above and all of the observations about the structure of the metadata hold the same. The only difference is clearly the cell line which is now HCC1806.

We continue by taking a look at the database itself. Immediately, we notice the sparsity we saw before and the big differeence between the expression levels of some genes so a log transformation may again be needed. Also a normalization seems to be required in order to homogenise the read counts between the cells in order to prevent any biases due to cells that are sequenced deeper and have more reads. Again the structure is the one we have already familiarized ourselves with above, so there is not much more to be done.

Looking at the shape or rather the dimensions of our data we see that they are not the same as in the SmartSeq MCF7 case. The sample is smaller at 243 cells while the features are more at 23396.

Again we look at the rows and the columns and the results are the same as in the Smartseq MCF7 case.

Now we take a look at the details of the database. Again, the results are similar to the Smartseq MCF7 case.

Next, we check for missing values. Again, in this case everything is alright so we leave the dataset as it is for now.

Taking a look at the variance of the genes, again we see a great spike at around 0 and a long tail to the right. This spike sugests that a great majority of the genes are mainly sparse and or are "housekeeping" genes that are relatively constant among the cells. The same as in the previous dataset we may want to filter out such genes and leave the ones with higher variance as they would likely be the ones that would provide the best model. This way we only keep the most useful while simplifying the dataset and respectively our model.

Just as above, a log plot would better show us the underlying distribution. Where we see a similar curve as before, that, disregarding the spike, starts off lower, raises and falls again with a long tail to the right.

Moving on to the analysis of the total read counts, gene expression count and mitochondrial percentage of the cells, we notice that in this dataset when looking at the plots we see that the distribution of cells is such that there are much fewer cells with low gene expression counts and low read counts. In the latter there isn't a big spike arround 0, but spikes/clusters of cells at different read counts over 500 000. Lastly looking at the mitochondrial percentage, the situation seems to be similar to the former case. All the three plots suggest that in this case there are less cells of low quality that we would otherwise remove, a fact which may be attributed to technological advancements or better cell collection. This is a good sign as this dataset has less cells overall so we would like to keep as many of the cells as possible in order to get a well trained model.

We can also do plots that will visualize whether the data is normalized. Again it is clearly not, neither the samples nor the features which would lead to difficulties with models if left unchanged.

## DropSeq

It is important to note most of what is done below is similar to the steps above, so less explanation will be given.

#### MCF 7

Reading the dataset and showing the first 5 rows, we see that the overall expression counts per gene seem to be lower which is expected given the more shallow sequencing method.

Here, we want to show the distribution of total different genes present in each cell by filtering the positive values from the dataframe.

Our dataset also needs to be checked for the total number of genes present in each cell, because filtering the cells that have less than 70 genes might help us in reducing our feature number.

At this point, we will also plot the histogram for the percentage of the Mitochondria present in each cell.

We also want to discover whether there is a linear relationship between the number of different genes and the total number of genes in a cell.

In this section, we want to look at the most and the least "popular" genes in our dataset.

Proceeding, we will compute the variance of each gene and extract the ones with a variance lower than 1%

Something else we found important to do was to check how many Hypo and Norm cells we had, to make sure we had enough supports for both cases.

To identify what the 10 genes with the highest total expression in normoxia and hypoxia conditions are respectively, we decided to proceed as shown below:

One interesting thing to note is that a few of those highly expressed genes appear in both cases.

While not a revolutionary statement by any means, we notice we are dealing with highly sparse data.

As recommended in the report suggestions, we also decided to take a look at the skewness and the kurtosis of the data, as can be seen below:

To check for redundancy and independence, we also decided to take a look at the correlation heatmap of the top 50 most expressed genes.

At this point, it is worth noting that even from a purely visual sense, it truly is incredibly interesting to study cells and genes using computational tools. From a practical point of view, however, to get back to the meat of the project, we see that many of the top values are correlated, something to keep in mind when we proceed with our model.

Violin plots below, to explore the density of our data:

We confirm something established by the sparsity graph: the vast majority of our gene values are 0.

#### HCC 1806

##### Reading the dataset and showing the first 5 rows

Here, we want to show the distribution of total different genes present in each cell by filtering the positive values from the dataframe.

Following, our dataset also needs to be checked for the total number of genes present in each cell, because filtering the cells that have less than 70 genes might help us in reducing our feature number.

At this point, we will also plot the histogram for the percentage of the Mitochondria present in each cell.

We also want to discover wether there is a linear relationship between the number of different genes and the total number of genes in a cell.

In this section, we want to look at the most and the least "popular" genes in our dataset and do some filtering with them.

As for the last step, we want to explore the variance of each gene.

While most of the code and the conclusions are similar to the ones in MCF7 (which is why there aren't many comments), one thing to note is that in HCC1806, in comparison with MCF7, the cells with the most expression are the hypoxic ones.

# Data Preprocessing

## SmartSeq

#### SmartSeq MCF7 Unfiltered

The next crucial step in our analysis is to check for duplicates. They could result in double counting and skew the databaes in ways that do not accurately represent the true nature of the data. We check for duplicate cell names and gene names which would suggest an initial issue with our dataset that we need to fix. Also we check for duplicatate cell and gene profiles. We see that there are no two duplicate cell profiles so there are no two cells that have the same expression of each gene. We however see that there are duplicate gene expressions, so there are genes that have the same expression values across the cells. These genes are most likely 'maintenance' genes and will not provide any variance that could be used in models but in this case keeping them will not harm our analysis as is is representative of the true biological nature of the cells. If the duplicates however are the exact same gene but with different name, bias might be created if we decide to keep all instances of them. Still, such removal should be properly documented.

##### Quality Control

Next, we can perform some quality control on the cells. What we can do is to check the total read counts of the genes for each cell and discard cells under a certain thereshold. According to bioconductor.org a sutable threshold would be 100 000 total reads per cell. Any lower than that and we risk including damaged cells in our database and analysis which could lead to additional noise, obscuring the actual dependencies we are trying to find.

Additionally, we can also remove cells that express less than a certian amount of genes. as again this could indicate that the cell is damaged. According to bioconductor.org a suitable cut-off would be around 5000.

Lastly we look at the cells with high mitochondrial percentage. Again from the same source we filter out cells with mitochondrial percentage of over 10% as they are likely to be damaged. (i.e. cells in which over 10% of the reads come from mitochondrial genes are dicarded)

Now we remove the cells that are likely to be damaged.

What we do below is to double check that our thresholds are reasonable. For that we will make some plots that will help is with visualizing the numbers.

As we can see the three thresholds seem to be good. In the first and the last case we see that just the tails are cut off without digging into the "body" of the distribution itself. In the second case we see a spike around 0 and then a decrease before an increase starts again which suggests we have removed a cluster of "bad" cells around 0 while leaving the true distribution intact.

##### Normalization and Transformation

Now that we have finished the quality control we can move to the normalization and the transformation. It is crucial that this step is taken after we have removed the low quality cells as such "bad" cells would distort the scaling and could skew the mean and variance used in standardization. According to pmc.ncbi.nlm.nih.gov, Smart-seq and Drop-seq data will have different sequencing depths as Smart-seq typically has higher read depth per cell (full-length transcripts), while Drop-seq (UMI-based) has more cells but sparser counts. We need to normalize each to account for library size differences.  

One cell might have 1,000,000 total reads, another only 100,000.
Raw counts would:

- Bias models toward high-depth cells
- Distort comparisons
- Confound clustering/dimensionality reduction


After we have done the normalization we perform log-transform. That is because the dataset is quite sparse and also some genes are expressed with very high levels across most cells which may lead with issues down the line. For instance the highly expressed genes would dominate variance based methods like PCA. With the log transfrom we compress this range so the range of the possible expression values will become much smaller. This also improves variance stability and in general makes our gene-level distribution more model friendly.

##### Identifying High Variable Genes

Lastly we identify the high variance genes as these are the only ones that we will use during the training. The low variance genes likely do not provide and meaningful information about the underlying condition and would only introduce noise and difficulties in training.

#### SmartSeq HCC1806 Unfiltered

The next crucial step in our analysis is to check for duplicates. They could result in double counting and skew the database in ways that do not accurately represent the true nature of the data. We check for duplicate cell names and gene names which would suggest an initial issue with our dataset that we need to fix. Again, we get pretty much the same result as in the Smartseq MCF7 case so our observations apply here as well.

##### Quality Control

After that, we can perform some quality control on the cells. What we can do is to check the total read counts of the genes for each cell and discard cells under a certain threshold. According to bioconductor.org a suitable threshold would be 100 000 total reads per cell. Any lower than that and we risk including damaged cells in our database and analysis which could lead to additional noise, and obscuring the actual dependencies we are trying to find.

Additionally we can also remove cells that express less than a certain amount of genes, as this could indicate that the cell is damaged. According to bioconductor.org a suitable cut-off would be around 5000.

Lastly, we look at the cells with high mitochondrial percentage. Again from the same source we filter out cells with mitochondrial percentage of over 10% as they are likely to be damaged. (i.e. cells in which over 10% of the reads come from mitochondrial genes are discarded)

Now we remove the cells that are likely to be damaged.

What we do now is to double check that our thresholds are reasonable. For that we will make some plots that will help us with visualizing the numbers.

As we can see the three thresholds seem to to good. Again as in MCF7 we see that in the first and the last case just the tails are cut off without digging into the "body" of the distribution itself. In the second case however we don't see as large of a spike around 0 which suggests that more cells are of higher quallity.

##### Normalization and Transformation

Now that we have finished the quality control we can move to the normalization and the transformation. It is crucial that this step is taken after we have removed the low quality cells as such "bad" cells would distort the scaling and could skew the mean and variance used in standardization. 

One cell might have 1,000,000 total reads, another only 100,000. Such discrepancies can hinder the performance of models and give poor results and could: 

- Bias models toward high-depth cells
- Distort comparisons
- Confound clustering/dimensionality reduction


After we have done the normalization we perform log-transform. That is because the dataset is quite sparse and also some genes are expressed with very high levels across most cells which may lead with issues down the line. For instance the highly expressed genes would dominate variance based methods like PCA. With the log transform we compress this range so the range of the possible expression values will become much smaller. This also improves variance stability and in general makes our gene-level distribution more model friendly.

##### Identifying High Variable Genes

## DropSeq

#### DropSeq MCF7 Filtered

Now, we are going to remove all the cells that have less than 50 genes. These cells are likely damaged and of no interest.

Following, we can also remove the cells in which there are less than 70 genes present in total.

For the last step of the preprocessing of the columns, we need to find what is the percentage of mitochondria genes present in each cell. For the cells with a higher percentage than 10%, we will remove them.

Here, we apply the log transformation to reduce the sparsity in our dataset.

In this section, we want to look at the least popular genes in our dataset and keep only the ones that appear more than 50 times.

As for the last step, we aim at keeping all the genes that have a variance of 0.1 or higher.

#### DropSeq HCC1806 Filtered

Now, we are going to remove all the cells that have less than 50 genes.

Following, we can also remove the cells in which there are less than 70 genes present in total.

For the last step of the preprocessing of the columns, we need to find what the percentage of mitochondria genes present in each cell is. Cells with a mitochondrial gene percentage higher than 10% will be removed.

Here, we apply the log transformation to reduce the sparsity in our dataset.

In this section, we want to look at the least popular genes in our dataset and keep only the ones that appear more than 50 times.

As for the last step, we aim at keeping all the genes that have a variance of 0.1 or higher.

# Unsupervised Learning

In this next part of the analysis we move to using the already filtered, normalized and split data. Before we start with any type of learning we do some preparations of the databses such that we have a testing and a training set. These sets will be used throughout the learning.

In the unsupervised learning section of our code we will start by implementing a PCA on our datasets and then an unsupervised clustering algorithm. This is a good way to kick off the learning as both of these methods look at the underlying structure of the data without us pushing it to look towards a specific aspect such as the hypoxic or normoxic label. This has the potential to reveal how biologicaly different the two classes are and whether the biggest variance in our dataset is due to that difference precisely.

## DropSeq

### MCF7

#### PCA

Starting with the PCA on DropSeq MCF7 we transpose the predetermined training set, as most models expect samples as columns, and then split it into index values and the data values. The index values contain our labels so this is why we want to separate them. After that we perform a split again leaving 80% of the data to train on and 20 % of the data to test on.

When we look at the explained varainance form our 50 PCs we see a cumulative score of 65% which is not perfect by any means but it is good enough to be proceed further.

Here we simply extract the label from the index values and then turn the labels from strings to 0, 1 integers.

Plotting the data on our first two PCs we see that there is somewhat of a split of our data along our first pc, but the case is not so simple to be able to say that all of the variance in the first pc is because of the labels. Since we cannot plot the data in 50 dimensions, the best way to check whether there is a clearer split across all PCs is clustering.

#### Clustering

In this case we proceed with Hierarchical clustering. For clarity of the code we perform the split again but this time, instead of getting our top 50 principal components, we get enough so that the total explained variance is 80%. This is a good threshold to choose as there is still some dimensionality reduction, but we don't lose as much information and we leave 20% to be discarded which is not too bad as it can either be noise or, even if it is meaningful infromation, it is not enough to throw off our models.

Plotting the dendrogram, we see that the data has been divided into three clusters which is not as great of a result as we expected. This suggests that the biological differences are not as clear as we would have hoped for, but that does not mean that we won't be able to get better results down the line.

Below we will be performing the Agglomerative Clustering, coloring the data of the test set on our first two principal components based on the clusters and comparing to the graph below which is coloered according to the true labels. Interestingly, we observe that the general shape of the clustering is similar to the true values, but we can also see many dissimilarities and misclassified points.

Concluding the unsupervised learning of the DropSeq MCF7 dataset, we see that the data has some intrinsic biological differences between the two labels, but the difference is not clear enough to be able to rely just on it to train unsupervised models. There are also other differences that come into play which affect our results and hinder the performance of our models. For instance the hierarchical clustering discovered a third cluster even though in the data we have only two separating classes.

### HCC1806

Next, we continue with the unsupervised learning for the DropSeq HCC1806 dataset. Again, we do tranpsosing, splitting, but this time we also log transform the data. Such a transformation is often useful for methods like pca and clustering which are distance based methods, since too large of a scale for the features could introduce bias towards higher expression levels and cause poorer performance of our models.

#### PCA

Looking at the explained variance we see that in the first 50 components it is cumulatively less than on the MCF7 case as we reach just 36%. Of course that result is not necessarily bad, but it could suggest that the our main factor of difference in our cells (i.e the label) does not result in as prominent of a biological and genetic difference as initially expected. A low amount of explained variance however is not always necessarily a bad thing as it could potentally be related to precisely our classes while not including any of the noise and other biological differences.

Plotting that data on our first three principal components we see that the separation does not look too bad. There is mixing of the classes but there are also two relatively distinct clusters which could suggest a good performance with our clustering model.

#### Clustering

Again we proceed as in the DropSeq MCF7 case, by increasing principal components up to the point where we reach 80% explained variance.

Ploting the dendrogram, we see that the data has been divided into three cluster which is not as great of a result as we expected. This sugest that the biological differences are not as clear as we would have hoped for but that does not mean that we want be able to get better results down the line.

When comparing the results of the clusterin to the true labels, we see that the prediction does not look too good again confirming our belief that the true bilogical differences are more hidden away than in the MCF7 case and a stronger supervised model would be required for better result.

In conclusion of the undupervised learning of the DropSeq HCC1806 database, we could not find satisfying enough results. The first indicator was the low explained variance by the first 50 principal components but that by itself was not enough to conclude that the biological differences are not as clear. Performing the clustering however we see that the model is having quite a bit of trouble and not matching very well with the true labels.

## SmartSeq

### MCF7

#### PCA

We begin by doing principal component analysis. Although some feature selection has already been performed, we further decrease the dimension of our data. It will help reduce technical noise and emphasize the structured biological signal. It will also help with overfitting our models down the line. We first split our data into a test and train set to evaluate our prediction capacity.

Now we do the actual PCA. We will see the result by plotting our samples (i.e cells) on the PC1 vs PC2 scale and mark the Normal and Hypoxic cells with different colors. What we actually see is that the two different types of cells are quite clearly separated along PC1. This suggest that the most dominant source of variance (i.e PC1) is very associated with the difference between hypoxic cells. This suggest that we are moving in the right directian and there is actual systematic and biological expression difference between the two types of cells we want to classify. We also plot the PCs based on their variance ratio which tells us how much each one explains of the total

#### Clustering

Now that we have perfomed the PCA we can continue with the unsupervised learning with K-means clustering.

For our results above we see that the ARI index is very high at 0.941 and on the visualization we see great similarities between our clusters and the true labels with just a few points that are incorrectly classified. Since we have not used the labels in the training this result is not to be underappreciated as it shows that there are clear biological differences between the hypoxic and normoxic cells that our clustering model has managed to identify with the help of our PCA. We now move to check the result on a separate set (the test set) that has not been used in neither the PCA nor the K-means clustering model to further check the accuracy and generalizability of our model. We see that the ARI index is 1, meaning we have achieved perfect prediction which can be seen on the plots as well. At first it might seem strange that our performance on the test set is better than on the training set, but that can be explained by outliers that could have made their way into our train set and a bit of 'luck' in the splitting of the data so that no such outliers were present in our test.

### HCC1806

#### PCA

We begin by doing principal component analysis. Although some feature selection has already been performed, we further decrease the dimension of our data. It will help reduce technical noise and emphasize the structured biological signal. It will also help with overfitting our models down the line.

Now we do the actual PCA. We will see the result by plotting our samples (i.e. cells) on the PC1 vs PC2 scale and by marking the Normal and Hypoxic cells with different colors. In the case of the SmartSeq HCC1806 database we see that the cells are not divided as clearly as in the previous case. Not only that but even though the main variance between the cells by definition along the first principal component, we see that the clusters of hypoxic vs normoxic cells seem to be separated along the PC2 axis. This is a very interesting result that could suggest a few different things. One could be that simply due to outliers in our data, they have thrown off our PCA and thus the main principal component is not the one that separates the two different types of cells (as we would have assumed as it would make sense the main source of variance to be related to the two different classifiers). This scenario is quite plausible as we can see that the big majority of samples are on the left hand side but just a few are very far on the right. So the variance along PC1 could have been precisely caused by these few cells. Another reason might be that other differences between the cells are also prominent which would suggest that the cells could have another separating factor or factors that we are not aware of. Plotting the data on our second and third principal components we see that a clear border is still not present but the main direction of variance (now PC2) aligns with the direction that roughly separates the two classes of cells. Either way, the cut is less clear than in the MCF7 case which could suggest that in this dataset of cells the biological difference between the two classes is not as prominent and thus not picked out by the PCA. We will continue with doing the clustering on the first 30 PCs and a second time on the same PCs but excluding PC1. In both cases the data is normalized, standardized and log-scaled for maximum success of the PCA.

First we start by the K-means clustering on PC2 to PC30. We plot the data on the first two PCs but that is of not too great importance as we seek to compare the true labels vs the cluster labels. What we see is that the model is relatively successful but again, due to the unclear separation of the data, does poorer compared to the SmartSeq MCF7 case. Our Adjusted Rand Index is 0.64 where 1 is perfect and 0 is as good as random. The score is not terrible but a stronger model would be required for further improvement.

#### Clustering

Doing the model on all of the first 30 principal components we see that the results are much worse. The first principal component dominates the clustering and all of the values are labeled the same way. This clearly presents the issue that we tried to fix above of having a component that accounts for higher variance that is not aligned with our classifiers. As we can see, the model performs worse when we take into consideration the first PC.

Clearly, it is better to not use the first PC and this is why we perform the test on the training set with the clustering based on the PCs without the first one. We are getting a better score even than on the training set, but that could be due to a particularly lucky choice of training sample and not many samples in the training set. On the graph we can see that the clustering seems to separate the data quite closely as to how it is supposed to be separated and the ARI index confirms it.

# Supervised Learning

## Dropseq

### MCF7

We start with the Dropseq MCF7 case and we begin with a logistic regression. Our dataset is already normalized, which is important for this type of model, otherwise the results might be skewed. We see that the best performing parameters are {'C': 1, 'solver': 'lbfgs'}, and we get an accuracy of an average 97% over 5-fold cross-validation. This is a very good result and not too surprising given the relatively good performance of our dataset in unsupervised learning.

More specifically, we use a split on the training data (i.e. we split the training data that is given to us in the project). On the train split of the training data, we perform grid search and cross-validation to get the best model, and then we use that model to check its performance on data it has never seen (i.e. the test split of our training set).

#### Logistic Regression (97% ACCURACY)


#### K-Nearest Neighbors (94.5% ACCURACY)

#### Support Vector Machine and Kernel SVM (97% ACCURACY)

#### Kernel Support Vector Machine (97.5% ACCURACY)

#### Naive Bayes (82% ACCURACY)

#### Random Forest (94.6% ACCURACY)

### HCC1806

The situation with the DropSeq HCC1806 is quite similar, but we see that on average the models perform a bit worse than on the DropSeq MCF7. This again builds on to our observations during the unsupervised learning that this dataset is a bit more complex and the classes are not as clearly separated. As in the MCF7 case, our best performance is the Kernel SVM, but this time the increase in accuracy from the regular SVM is along the lines of 2%. This again is not too drastic but also suggests that the data is a bit less linearly separable in its original dimensions than the DropSeq MCF7 data.

From the confusion matrices in the models below, we see that all of the models perform similarly on the test set as they did during cross-validation, which again suggests no overfitting. This again is not too surprising given that we use cross-validation for training, which does not allow us to overfit too much.

#### Logistic Regression (94.5% ACCURACY)

#### K-Nearest Neighbors (92% ACCURACY)

#### Support Vector Machine (94.5% ACCURACY)

#### Kernel Support Vector Machine (95.5% ACCURACY)

#### Naive Bayes (93.5% ACCURACY)

#### Random Forest (94% ACCURACY)

## SmartSeq

### MCF7

Now we move to the SmartSeq MCF7 case. Here we see that we have quite a few models that give a 100% accuracy on the cross-validation and basically all models give a 100% accuracy on the training set. This is not too surprising given our results on this dataset during the unsupervised learning. We managed to get around 94% accuracy just with k-means clustering as our data was very linearly separable. Thus more complex supervised models manage to learn the distribution perfectly and get perfect results. What is interesting, however, in this case is that the Kernel SVM is one of the worst performing models in this dataset with 96% accuracy. Of course the accuracy is very high but the comparison with the SVM and other perfect models suggest that the data is so linearly separable in its natural dimensions that using a kernel only moves us away from that separability.

#### Logistic Regression (100% ACCURACY)

#### Support Vector Machine and Kernel SVM (100% ACCURACY)

#### Kernel Support Vector Machine (100% ACCURACY)

#### Naive Bayes (92% ACCURACY)

#### Random Forest (99% ACCURACY)

### HCC1806

Now we move to the SmartSeq HCC1806 case. Again we see very high accuracies of above 95% on most of the models. What is interesting is that again in the HCC1806 case, just like in DropSeq, the Naive Bayes model severely underperforms the others. This could be presenting some underlying biological feature of the HCC1806 cells given that we get similar results for both sequencing methods. In this case, the drop off in accuracy is much larger but this could also be due to the relatively smaller sample size in the SmartSeq datasets.

#### Logistic Regression (97.9% ACCURACY)

#### K-Nearest Neighbors (95% ACCURACY)

#### Support Vector Machine (98.6% ACCURACY)

#### Kernel Support Vector Machine (97.2% ACCURACY)

#### Naive Bayes (93% ACCURACY)

#### Random Forest (97.2% ACCURACY)

## Supervised Learning Conslusion

In conclusion of the supervised learning, we got very impressive results on each of the datasets. On both of the DropSeq cases, the best performance was achieved by the kernel support vector machine with an accuracy of 97.5% for the MCF7 cells and an accuracy of 94% in the HCC1806 cells. In the SmartSeq databases we got also amazing results, especially in the MCF7 case where we had multiple models with 100% accuracy. Specifically they were logistic regression, support vector machine, and random forest. In the HCC1806 case the best performing model was the logistic regression with 98.6% accuracy. What we also noticed is that on the SmartSeq method we managed to get higher accuracy than in the DropSeq case which suggests that deeper sequencing with fewer samples provides us more information about the underlying condition than more shallow sequencing with many samples.

# Conclusion

In conclusion, we started by exploring the data in all four datasets. We looked at important graphs and underlying structures of the data as well as the intrinsic biological meaning of the features and the samples as well as their distributions. This allowed us to get familiar with the structures of the datasets and their potential behavior during modeling. This revealed some changes that could be made so that everything could be more machine learning friendly and ready for training. This preprocessing included steps like duplicate checks, quality control, identification of high variance features, normalization and more. After that we moved on to the unsupervised learning where we used the pre-split and normalized training data given to us. We performed principal component analysis on all of the databases, which revealed information about the underlying biological structure for the data. For instance, in the MCF7 cases the highest variance components were also better at splitting the two classes of our cells which suggested that a lot of the variance was coming from exactly that difference in label. In the HCC1806 cases the separation was less clear and less variance could be explained by the principal components which suggested that the intrinsic biological differences were not as clear and less subtle. We finished the unsupervised learning with clustering which confirmed our PCA observations and performed best on the MCF7 cases and specifically very well on the SmartSeq MCF7 case suggesting good linear separability. The SmartSeq cases seemed to perform better than the DropSeq cases while MCF7 cells seemed to perform better than HCC1806 cells. After that our analysis moved to the supervised learning of the datasets. We tested the models SVM, KNN, kernel SVM, logistic regression, Naive Bayes, and Random Forest, where on average the best results were achieved by the SVMs and the Kernel SVMs. More specifically in the DropSeq cases we got 97.5% accuracy for MCF7 and 94% accuracy for HCC1806 and in both cases with the kernel SVM. In the SmartSeq case we get 100% accuracy by multiple models including SVM on the MCF7 case and 98.6% accuracy on the HCC1806 case again with SVM. All models were tested with grid search for parameter optimization and 5-fold cross-validation for overall performance.

Finally, our predictions were made by the following models (trained on the whole training sets):

DropSeq MCF7: Kernel SVM ('C': 100, 'gamma': 0.001, 'kernel': 'rbf')

DropSeq HCC1806: Kernel SVM ('C': 1, 'gamma': 'scale', 'kernel': 'rbf')

SmartSeq MCF7: SVM ('C': 0.01, 'kernel': 'linear')

SmartSeq HCC1806: SVM ('C': 0.01, 'kernel': 'linear')