## Introduction
This project contains R scripts for analyzing RNA-Seq data from 33 different cancer types obtained from the TCGA (The Cancer Genome Atlas) project. The analysis includes data normalization, transformation to TPM (Transcripts Per Million), and visualization through heatmaps and bar plots.

## Data
The RNA-Seq data is sourced from TCGA projects. The datasets are accessed using the recount3 package, which provides a structured way to work with genomic data.

## STEPS FOR ANALYSIS:
1. Load the required libraries
2. Retrieve all available projects and filter the projects that are specifically from TCGA data sources
3. Process each TCGA project to create 'RangedSummarizedExperiment' objects
4. Extract gene information and access metadata
5. Specify genes of interest related to cancer
6. Normalize raw counts to TPM using a custom function
7. Combine metadata 
8. Create a final data frame by combining the TPM matrix and metadata

## Visualization
• Generate a heatmap to visualize the expression data of the specified cancer-related genes across different cancer types
• Perform a sanity check to ensure the biological relevance of the results using a subset of genes 
• Scale the expression values for each gene across cancer types and generate a scaled heatmap for comparative visualization



 