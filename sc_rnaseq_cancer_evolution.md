# What Single-Cell Data is Teaching Us About Cancer Evolution

**Connect scRNA-seq to tumour heterogeneity and therapy resistance.**

---

## Introduction

Clonal evolution (CE) model describes tumor progression through sequential genetic mutations in individual cells, analogous to Darwinian evolution, where diversification and selection based on cellular fitness lead to the emergence of dominant, more malignant subpopulations. The model has advanced in parallel with improvements in sequencing technologies, deepening our ability to observe genetic and transcriptomic heterogeneity in tumours [1].

RNA sequencing methods have progressed rapidly from bulk RNA-seq, to laser-capture micro-dissection, single-cell RNA-seq, and more recently spatial transcriptomics. This evolution of technology has revealed that cancer does not evolve by a single linear clone. Instead, multiple subclones often emerge and coexist, sometimes due to similar fitness or spatial separation, and can even complement each other’s survival. Clonal architecture varies substantially between individual tumours of the same type. In response, computational and experimental methods continue evolving to better model clonal dynamics and inform treatment strategies [1,3].

---

## Transition from Bulk RNA-seq to scRNA-seq

Bulk RNA-seq has been foundational in cancer genomics, helping to classify molecular subtypes, measure gene-expression changes associated with mutations, and discover biomarkers. However, bulk RNA-seq averages the transcriptomes of all cells in a sample, masking the contribution of rare or distinct cell populations.

To overcome this limitation, **single-cell RNA sequencing (scRNA-seq)** was developed. scRNA-seq enables transcriptomic profiling at the resolution of individual cells, which allows detection of rare cell types, intermediate states, and cellular dynamics. RNA sequencing has progressed to single-molecular, single-cell, and spatial transcriptome approaches, improving accuracy of cell-level resolution and contributing to our understanding of cancer heterogeneity and evolution [2,3].

---

## Uncovering Tumour Heterogeneity with scRNA-seq

Cancer exhibits extensive transcriptional heterogeneity, reflecting differences in proliferation, differentiation, immune evasion, and drug response [4,5]. This variability arises from genetic mutations as well as non-genetic mechanisms, including epigenetic modifications, stochastic gene expression, and signals from the tumour microenvironment such as hypoxia, cytokines, or interactions with stromal and immune cells [6,7,11]. For instance, connective tissue cells and infiltrating immune cells can modulate gene expression in cancer cells, promoting invasion and resistance [8].

Single-cell RNA sequencing (scRNA-seq) is essential for dissecting these layers of complexity. By profiling individual cells, scRNA-seq uncovers rare cell populations, intermediate states, and developmental trajectories that are obscured in bulk analyses [9,10,13]. Tumour cells from the same patient may display divergent transcriptional programs, including proliferative, quiescent, epithelial-to-mesenchymal transition (EMT), stress-response, or drug-tolerant states [12,14].

Trajectory analyses, pseudotime reconstruction, and dimensionality-reduction techniques (e.g., UMAP, t-SNE) reveal transitions between states, including EMT and drug-tolerant phenotypes [12,14]. When combined with spatial transcriptomics, scRNA-seq additionally maps how transcriptional programs are organized within the tumour and influenced by local microenvironmental interactions [15]. This approach highlights the contributions of both genetic and non-genetic heterogeneity to tumour progression, plasticity, and therapy response.

---

## Tracking Cancer Evolution with scRNA-seq

scRNA-seq has also enabled the reconstruction of tumour evolutionary dynamics at single-cell resolution [14]. By profiling thousands of cells simultaneously, researchers can trace differentiation hierarchies, identify stem-like and drug-resistant subpopulations, and map transcriptional trajectories associated with metastasis or therapy adaptation. Unlike bulk RNA-seq, which averages signals across millions of cells, scRNA-seq reveals coexisting subclones and dynamic state transitions, providing a more accurate depiction of tumour evolution [12,14].

Genetic inference from scRNA-seq data such as detection of copy-number alterations (CNAs), expressed somatic mutations, and mitochondrial DNA variants allows subclonal reconstruction and phylogenetic mapping [16,17,18]. Computational tools like **inferCNV**, **CopyKAT**, and **SCEVAN** assign cells to likely genomic lineages, while experimental lineage-tracing approaches, including CRISPR-based barcoding, enhance clonal tracking in model systems [16].

Integration with complementary single-cell modalities, including single-cell DNA sequencing, ATAC-seq, and spatial transcriptomics, links genotype to phenotype, connecting transcriptional reprogramming to genetic diversification and microenvironmental adaptation [12,15]. Together, these methods provide a dynamic view of cancer as an evolving ecosystem, allowing identification of drug-resistant subclones before they expand and informing precision therapies designed to anticipate and disrupt tumour evolution [17].

---

## Connecting scRNA-seq to Therapy Resistance

Because genetic and epigenetic differences between tumours of the same type in different patients can lead to drug resistance and therapeutic failure [16], integrating drug response data with scRNA-seq enables analysis at single-cell resolution and the identification of therapeutic clusters. Before **Beyondcell**, there was no computational method capable of inferring drug sensitivity from single-cell gene expression combined with high-throughput drug screening. With the Beyondcell approach, tumour responses to treatment can be monitored across different cellular subpopulations using scRNA-seq [17]. Studies have shown that scRNA-seq contributes to more effective therapies in various cancers, including glioblastoma, which previously yielded less accurate results [18].

---

## Challenges and Future Perspectives

A major limitation of single-cell RNA sequencing (scRNA-seq) in solid tumours is that samples must be dissociated into viable single cells before sequencing. The mechanical and enzymatic steps used for dissociation often trigger stress responses that alter transcription and add technical noise, making it hard to tell whether gene-expression differences come from real tumour heterogeneity or from sample handling [19].

Because fresh material is usually required, collecting multiple or serial biopsies from the same patient is also difficult, which limits studies of tumour evolution over time. Some groups work with organoids or cell lines to avoid this problem, but those models do not fully reproduce interactions with the tumour microenvironment. Even with improvements such as single-nucleus RNA-seq and fixation-compatible workflows, technical noise and sampling bias still restrict the accuracy and clinical use of scRNA-seq in cancer research [20,21]. Optimising fixation and storage protocols could greatly expand the clinical application of scRNA-seq, allowing more flexible sample handling and improving the study of tumour heterogeneity. Widespread implementation of these methods may enhance our ability to track cancer evolution and guide therapeutic strategies.

---

## References

1. Wang, Y., et al. (2020). *Changing technologies of RNA sequencing and their applications in clinical oncology.* Frontiers in Oncology, 10, Article 447.  
2. Hong, M., et al. (2020). *RNA sequencing: new technologies and applications in cancer research.* Journal of Hematology & Oncology, 13, Article 166.  
3. Jiang, L., et al. (2016). *GiniClust: detecting rare cell types from single‑cell gene expression data with Gini index.* Genome Biology, 17, Article 144.  
4. Patel, A. P., et al. (2014). *Single-cell RNA-seq highlights intratumoral heterogeneity in primary glioblastoma.* Science, 344(6190), 1396–1401.  
5. Tirosh, I., et al. (2016). *Dissecting the multicellular ecosystem of metastatic melanoma by single-cell RNA-seq.* Science, 352(6282), 189–196.  
6. Neftel, C., et al. (2019). *An integrative model of cellular states, plasticity, and genetics for glioblastoma.* Cell, 178(4), 835–849.e21.  
7. Zhang, L., et al. (2021). *Single-cell transcriptomics reveals the landscape of intratumoral heterogeneity and transcriptional plasticity in liver cancer.* Nature Communications, 12, 7279.  
8. Keren, L., et al. (2018). *A structured tumor-immune microenvironment in triple negative breast cancer revealed by multiplexed ion beam imaging.* Cell, 174(6), 1373–1387.e19.  
9. Stuart, T., & Satija, R. (2019). *Integrative single-cell analysis.* Nature Reviews Genetics, 20(5), 257–272.  
10. Suvà, M. L., & Tirosh, I. (2023). *Cancer cell state plasticity as a driver of tumor evolution and therapy resistance.* Cancer Cell, 41(5), 563–577.  
... *(continue numbering all references through 37)*

---

## Contributors

- Özlem Kalkan  
- Oni David Sunday  
- Ayşenur Akcan  
- Daria Kriuchkova  
- Noor Ul Ain Amir  
- Minenhle Mayisela

