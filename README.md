
# Complete Categories of DNA Sequencing (DNA‑seq) Analysis

This document provides a **comprehensive, exhaustive classification** of all categories under **DNA sequencing analysis**.  
It is intended as a reference for learning, teaching, or building full bioinformatics workflows.

---

# 📌 Overview

DNA‑seq analysis focuses on extracting biological and clinical meaning from **DNA reads** produced by sequencing platforms (Illumina, ONT, PacBio).  
It does *not* include RNA‑seq, epigenomics, or proteomics.

Below are **all major categories** of DNA sequencing analysis used in modern genomics.

---

# 🧬 1. Basic DNA Sequence Analysis

These analyses are independent of NGS machines and work directly on sequences.

### Includes:
- GC content, AT/GC skew  
- Reverse complement  
- K-mer counting  
- Motif detection  
- Sequence alignment (local, global, MSA)  
- ORF detection & gene prediction  
- Phylogenetic tree building  

### Used for:
- Gene characterization  
- Evolutionary studies  
- Algorithmic bioinformatics  

---

# 🧬 2. Raw NGS Data QC & Preprocessing

### Includes:
- FASTQ QC (FastQC)
- Adapter trimming
- Low-quality base removal
- Read filtering
- Contamination detection

### Used for:
- All downstream DNA‑seq workflows  

---

# 🧬 3. Read Mapping & Alignment

Mapping sequencing reads to a reference genome.

### Includes:
- Aligners (BWA, Bowtie2, minimap2)
- SAM/BAM processing (sort, index)
- Duplicate marking
- Alignment QC (flagstat, stats)

### Used for:
- Variant calling  
- Comparative genomics  
- WGS, WES, Panels  

---

# 🧬 4. Variant Calling (SNVs & Indels)

Core DNA‑seq category. Detects **point mutations** and **small insertions/deletions**.

### Includes:
- Germline variant calling
- Somatic variant calling  
- Low-frequency mutation detection  
- VCF generation
- Variant filtering
- Variant annotation (VEP, Annovar)

### Used for:
- Human genetics  
- Cancer genomics  
- Rare disease diagnostics  

---

# 🧬 5. Structural Variant (SV) Analysis

Detects **large genomic changes (>50 bp)**.

### Includes:
- Deletions  
- Insertions  
- Duplications  
- Inversions  
- Translocations  

### Tools:
- Manta  
- Lumpy  
- Delly  
- SvABA  

---

# 🧬 6. Copy Number Variant (CNV) Analysis

Detects changes in **gene or region copy number**.

### Includes:
- Gains  
- Losses  
- Amplifications  
- Genome-wide CNV profiling

### Tools:
- CNVkit  
- Control-FREEC  
- GATK gCNV  

### Used for:
- Cancer  
- Developmental disorders  

---

# 🧬 7. Whole Genome Sequencing (WGS)

Sequencing the entire genome.

### Resolution:
- Detects: SNVs, indels, SVs, CNVs, hotspots  
- Can be short-read or long-read  

### Used for:
- Population genomics  
- Clinical diagnostics  
- Evolutionary biology  

---

# 🧬 8. Whole Exome Sequencing (WES)

Sequences only coding regions (~2% of genome).

### Includes:
- Exome capture QC  
- Exon-level depth analysis  
- Exonic variant interpretation  

### Used for:
- Clinical genetics  
- Disease gene discovery  

---

# 🧬 9. Targeted / Panel Sequencing

Select genes are sequenced at **very high depth**.

### Includes:
- Cancer panels  
- Pharmacogenomics  
- Carrier screenings  

### Deliverables:
- Variant calling  
- Clinical reporting  

---

# 🧬 10. De Novo Genome Assembly

Build a genome **without a reference**.

### Includes:
- Short-read assembly (SPAdes)  
- Long-read assembly (Flye, Canu)  
- Hybrid assembly  
- Polishing (Pilon, Racon)  

### Used for:
- New species  
- Bacterial genome assembly  
- Viral genome builds  

---

# 🧬 11. Reference Genome Improvement / Polishing

Improving an existing genome assembly.

### Includes:
- Gap closing  
- Error correction  
- Scaffolding  
- Haplotyping  

### Tools:
- Pilon  
- Racon  
- Medaka  

---

# 🧬 12. Comparative Genomics

Comparing genomes across species or strains.

### Includes:
- Whole-genome alignment  
- Synteny analysis  
- Pangenome generation  
- Variant comparisons  

### Tools:
- Mauve  
- MUMmer  
- Minimap2  

---

# 🧬 13. Pangenomics

Combines multiple genomes into a single representation.

### Includes:
- Core vs accessory genome analysis  
- Graph genomes (GFA)  
- Strain-level comparison  

### Tools:
- Panaroo  
- Roary  
- PGGB  

---

# 🧬 14. Microbial Variant & Strain Typing

Used for epidemiology, AMR, and outbreak studies.

### Includes:
- MLST  
- SNV pipelines (Nextstrain-style)  
- AMR gene detection  
- Plasmid detection  

### Tools:
- Abricate  
- MLST  
- Snippy  

---

# 🧬 15. Viral Genome Analysis

Specialized DNA/RNA viral workflows.

### Includes:
- Consensus calling  
- Lineage classification  
- Mutation tracking  
- Quasispecies analysis  

### Tools:
- iVar  
- Nextclade  
- Pangolin (for SARS‑CoV‑2)  

---

# 🧬 16. Methylation‑Calling from DNA (Long Reads)

Even though epigenomics is separate, ONT/PacBio can measure methylation **natively from DNA reads**.

### Includes:
- CpG methylation detection  
- Motif-level methylation  

### Tools:
- Nanopolish  
- F5C  
- Megalodon  

---

# 🧬 17. Quality Assurance, Validation, and Reporting

Final step in clinical/regulatory pipelines.

### Includes:
- Coverage QC  
- Depth of target regions  
- Sensitivity/specificity  
- Clinical variant classification (ACMG)  

---

# 📌 Complete Category Map

| Category | Focus |
|---------|-------|
| 1 | Basic sequence-level analysis |
| 2 | NGS raw data QC |
| 3 | Read mapping |
| 4 | Variant calling (SNVs/indels) |
| 5 | Structural variant calling |
| 6 | CNV analysis |
| 7 | WGS |
| 8 | WES |
| 9 | Targeted panels |
| 10 | De novo assembly |
| 11 | Genome polishing |
| 12 | Comparative genomics |
| 13 | Pangenomics |
| 14 | Microbial/strain typing |
| 15 | Viral genomics |
| 16 | Methylation from DNA reads |
| 17 | Clinical/QA reporting |

This is the **full exhaustive list** of categories inside DNA‑seq analysis.

---

# 📘 Author

Your Name  
GitHub: your‑github‑profile  
License: MIT
