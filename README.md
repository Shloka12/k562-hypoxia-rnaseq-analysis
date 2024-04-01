# Transcriptomic Analysis of K562 Cells Under Hypoxic Conditions: Insights into Mitochondrial Function

## Overview

This project aims to explore the effects of low oxygen (hypoxia) on RNA transcript levels in K562 cells. Hypoxia is of particular interest due to its central role in the function of mitochondria and its potential therapeutic applications in mitochondrial diseases such as Leigh Syndrome.

## Dataset

The provided dataset consists of bulk RNA-seq time course data from K562 cells cultured under the following conditions:

- Room air (21% oxygen)
- Moderate hypoxia (5% oxygen)
- Strong hypoxia (1% oxygen)

Samples were collected at four time points: 6 hours, 24 hours, 3 days, and 6 days. Each condition has three replicates.

The data is provided in a table format (`GSE144527_gene_fpkm.txt`), where each row corresponds to a gene and each column corresponds to a sample. Gene expression levels are given in units of fragments per kilobase per million (FPKM), which are already normalized for gene length and sequencing depth.

## Supplementary Data

Two additional gene lists are provided to aid in the analysis:

1. `benita_2009_hif1a_targets.cleaned.csv`: A list of genes that are targets of HIF-1α, a key transcription factor in the cellular response to hypoxia.

2. `Human.MitoCarta3.0.lite.csv`: A table of information about mitochondrial genes from MitoCarta3.0.

## Analysis Tasks

1. Data cleaning:
   - Remove genes with extremely low expression across all samples.
   - Log-transform FPKM values to reduce the influence of outliers.
   - Generate a histogram plot to choose a reasonable threshold for excluding low-expression genes.

2. Analysis of the day 6 time point:
   - Run a principal components analysis (PCA) on the data.
   - Create scatter plots of the first few components to assess if any component separates samples by oxygen status.
   - Identify the top 25 differentially expressed genes for both hypoxia levels.
   - Determine the overlap between the differentially expressed genes and the list of HIF-1α targets.
   - Investigate whether mitochondrial genes tend to be up-regulated or down-regulated in hypoxia.

3. Incorporation of other time points:
   - Create a heatmap of the entire cleaned dataset, with genes as rows and samples as columns.
   - Normalize gene expression by row and order the genes by expression on day 3 at 1% oxygen.
   - Analyze the heatmap to gain insights into the dynamics of the transcriptomic response to hypoxia.

4. Suggest follow-up experiments based on the results.

## Conclusions

After performing the requested analyses, the following conclusions can be drawn:

1. Principal components analysis revealed that the first principal component separates samples by oxygen status, indicating that hypoxia has a significant effect on the transcriptome of K562 cells.

2. A substantial number of differentially expressed genes under hypoxia were found to be HIF-1α targets, suggesting that HIF-1α plays a crucial role in the cellular response to low oxygen conditions.

3. Mitochondrial genes were generally up-regulated in hypoxia.

   <img width="472" alt="image" src="https://github.com/Shloka12/k562-hypoxia-rnaseq-analysis/assets/67782856/7c449fd2-eed1-4a89-9b51-96c1a6fb47db">


4. The heatmap analysis revealed dynamic changes in gene expression over time, with some genes showing rapid responses to hypoxia and others exhibiting delayed or sustained changes.


<img width="518" alt="image" src="https://github.com/Shloka12/k562-hypoxia-rnaseq-analysis/assets/67782856/505388e4-6a48-4746-b6ce-f5a52dd81dfa">


These findings provide valuable insights into the transcriptomic response of K562 cells to hypoxia and highlight potential avenues for further investigation, such as studying the functional consequences of the observed gene expression changes and exploring the therapeutic potential of hypoxia in the context of mitochondrial diseases.

