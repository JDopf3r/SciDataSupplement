## Supplementary Code for the *Nature Scientific Data* Manuscript by Dopfer et al.

**Created:** December 2024 (J. Dopfer)  
**Website:** [tracerdb.org](https://tracerdb.org)  
**Contact:** [info@tracerdb.org](mailto:info@tracerdb.org)  

---

### Manuscript Details

This repository provides supplementary information for the manuscript:

**"Insights into a Curated Database for Fluorescent Tracers to Accelerate Assay Development."**

---

### Overview of the Repository

**`data_visualization.ipynb` Script**:  
  This script outlines the pipeline used for data visualization in our [data explorer](https://tracerdb.org/overview/). The pipeline leverages high-dimensional embeddings of kinase domains, which were compressed using a vanilla autoencoder architecture.

**`model_training.ipynb` Script**:  
  This script documents the autoencoder architecture and the training procedure used for compressing the kinase domain embeddings.

### **`Data` Directory**

1. **[Human Proteome FASTA](Data/UP000005640_9606.fasta)**:  
   Sourced from [UniProt](https://www.uniprot.org/proteomes/UP000005640), this file contains the full human proteome in FASTA format.

2. **[Per-Protein Embeddings](Data/protein_embeddings_uniprot.h5)**:  
   Derived from the *prottrans_t5_xl_u50* protein language model, these embeddings are available from [UniProt](https://www.uniprot.org/help/downloads).

3. **[HMMscan Results](Data/proteome_hmmer_results.out)**:  
   Contains domain annotations for all protein sequences within the [human proteome FASTA](Data/UP000005640_9606.fasta).

4. **[Proteome DataFrame](Data/proteome.parquet)**:  
   Stores additional metadata used for the classification of human proteins.



Due to the large file size (3.7 GB each) of the two autoencoder parameter files, they are **not included** in this repository. Instead, these files, along with the DataFrame containing the learned latent embeddings for the kinase domains, are available in the data repository on **figshare**.

---

### Running the Visualization Locally

To run the kinase domain visualization locally, you will need to:

1. **Download the per-residue embedding file** from [UniProt](https://www.uniprot.org/help/downloads).
2. **Place the downloaded file** in the `Data` directory.
3. **Execute the [script](data_visualization.ipynb)** 

---

For any questions or issues, please reach out via [info@tracerdb.org](mailto:info@tracerdb.org).
