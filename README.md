# Joint Modeling

This repository contains all the code files for the joint modeling project. All datasets are contained in the Google Drive, available [here](https://drive.google.com/drive/folders/1i5rAf609xfcu-4Zt5SEVdLaNm4sTqgtu?usp=share_link).

## Code Explanation:

- `Sequenc_clean`: This folder contains all the cardio single-cell RNA sequencing data, including data import, cleaning, visualization, PCA, and clustering using the original `seurat package`.

- `scanoroma_celltypecluster`: Utilizes the `scanoroma` method to cluster and determine the cell types of cardio cells. It includes PCA, clustering, and UMAP using the scanoroma method. Cell type annotation and marker analysis with a dot plot of the top 10 markers are also contained in this file.

- `spatial_clean`: This folder contains all the cardio single-cell transcriptomics data. The transcriptomics data are imported, cleaned, processed through PCA, and clustered using methods from both `seurat` and `scanoroma`. Anchor finding is performed to link the single RNA sequencing data and transcriptomics data. Prediction scores are calculated for each location spot to determine the spot cell type.

- `spatial_TMSB4X expression`: Connects single RNA sequencing data with single RNA transcriptomics data. Performs spatial visualization of cell types. Extracts the TMSB4x highly-expressed cell cluster, and produces differential genes expressed in anatomical regions, as well as differential genes expressed at various time points.

- `LMM`: Contains the linear mixed model fitting on the single RNA sequencing data.

- `Cox_visual`: Offers the visualization of the spatial transcriptomics data using the `spatstat package`.

- `cox_spatial_tm`: This code first models the sequencing data using the LMM model, and then pipes the LMM result into the Cox spatial model.

- `temporal`: Constructs the Cox spatial-temporal model on the transcriptomics data.

