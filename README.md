## RNA-Seq Analysis of Hypoxia vs Normoxia Conditions
# Introduction
This repository contains R scripts for analyzing RNA-Seq data to identify gene expression changes under hypoxia and normoxia conditions in the SW480 cell line. This analysis includes data normalization, differential expression analysis, visualization, and pathway analysis.
# Data
The RNA-Seq data is in the .tsv format and was obtained from the GEO database. For this analysis, we used the dataset GSE197576.

# STEPS FOR ANALYSIS:
# Data Loading and Preprocessing
•  Load the required libraries.
•  Read the raw counts data from the .tsv file.
•  Subset the data to include only the relevant samples.
•  Convert the data to a matrix format and set row names to gene names.

# Calculate Total Exon Length Per Gene
•  Load the TxDb.Hsapiens.UCSC.hg19.knownGene package to obtain exon information.
•  Calculate the length of exons and sum them up per gene.
•  Map the ENTREZID to official gene symbols using the org.Hs.eg.db package.
•  Subset the data to include only common genes between the raw counts matrix and the mapping table.

# Normalizing Raw Counts to TPM
•  Create a function to normalize the raw counts to Transcripts Per Million (TPM).
•  Apply the TPM function to the data.

# Differential Expression Analysis with DESeq2
•	Create a DESeqDataSet object from the raw counts matrix.
•	Perform differential gene expression analysis using DESeq2.
•	Generate a volcano plot to visualize significant changes in gene expression.
•	Identify and label significant genes on the volcano plot.

# Visualization
•	Perform variance stabilizing transformation (VST) on the data.
•	Plot PCA to visualize sample clustering.
•	Generate a heatmap with scaled data to visualize patterns. 

# Pathway Analysis
•  Convert gene symbols to Entrez IDs.
•  Perform Gene Ontology (GO) enrichment analysis using clusterProfiler.
•  Retrieve Hallmark gene sets for Homo sapiens using msigdbr.
•  Perform gene set enrichment analysis (GSEA) using pre-ranked gene lists and reference gene sets.
•  Visualize pathway analysis results using bar plots and dot plots.

