# **Mouse Atlas Project**
This repository contains scripts and data for creating a Mouse Atlas by integrating datasets from the small and large intestines.

## **Files and Scripts**
**Mouse Atlas Data Mining.xlsx**: Lists all datasets to be integrated for the Atlas.
**Individual_datasets_analysis.Rmd**: Contains scripts for quality control and annotation of each dataset.

## **Integration Methods**
Various integration methods have been evaluated:

Scanvi, Scanorama, and scVI are recommended for complex integrations.
Harmony is suitable for simpler integrations but may require parameter adjustments for more complex datasets.
Refer to the benchmark paper for more details: Luecken, M.D., Büttner, M., Chaichoompu, K. et al. Benchmarking atlas-level data integration in single-cell genomics. Nat Methods 19, 41–50 (2022). DOI: 10.1038/s41592-021-01336-8

Scanvi, scanorama and scvi re recommended fro more complex integrations while Harmony works fine for more simple ones.

For performance comparison of methods, see: **Scib_integration_tests.ipynb**

## **Results**
For integration of datasets obtained from the Large Intestine Scanvi performed best overall, followed by Scanorama.
![Benchmark plot](Images/LI_benchamark_plot.png)
![Umap per method comparison](Images/LI_umap_comparison_methods.png)

When additional two datasets from the small intestine were added:
Scanvi remained the best, while Scanorama dropped to third place. Harmony was effective with standard parameters but less so with the small intestine datasets. Further tuning was needed.

![Benchmark plot](images/Images/SI_LI_benchmark_plot.png)
![Umap per method comparison](Images/SI_LI_Umap_comparison_tweaked_harmony.jpeg)



