
# DNA Analysis Pipeline – Example Project

This repository contains a complete small-scale DNA sequence analysis workflow using
a tiny real sequencing dataset (*E. coli*) suitable for learning QC → trimming → alignment → variant calling.

---

## 📁 Project Structure

```
dna_project/
├── data/
│   ├── raw/                 # raw FASTQ files
│   ├── trimmed/             # trimmed reads
│   ├── aligned/             # SAM/BAM files
│   ├── variants/            # VCF files
│   └── ref/                 # reference genome
├── scripts/
│   ├── 01_fastqc.sh
│   ├── 02_trim.sh
│   ├── 03_align.sh
│   ├── 04_sort_index.sh
│   ├── 05_variant_call.sh
│   ├── 06_python_analyze.py
│   └── 07_R_plot.R
└── results/
```

---

## 🧬 Input Data Used

### Example small dataset (3 MB):
**ERR458493.fastq.gz** (E. coli sequencing reads)

Download:

```
wget ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR458/ERR458493/ERR458493.fastq.gz
```

Reference genome:

```
wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/005/845/GCF_000005845.2_ASM584v2/GCF_000005845.2_ASM584v2_genomic.fna.gz
gunzip GCF_000005845.2_ASM584v2_genomic.fna.gz
mv GCF_000005845.2_ASM584v2_genomic.fna reference_ecoli.fasta
```

---

## 🔧 Dependencies

Install the required tools:

```
sudo apt install fastqc bwa samtools freebayes cutadapt python3-pandas r-base
```

---

## 🚀 Workflow Steps

### 1. Quality check (FastQC)

```
bash scripts/01_fastqc.sh
```

### 2. Trimming (Cutadapt)

```
bash scripts/02_trim.sh
```

### 3. Alignment (BWA)

```
bash scripts/03_align.sh
```

### 4. Sort & Index (Samtools)

```
bash scripts/04_sort_index.sh
```

### 5. Variant Calling (FreeBayes)

```
bash scripts/05_variant_call.sh
```

### 6. Python Analysis

```
python3 scripts/06_python_analyze.py
```

### 7. Visualization in R

```
Rscript scripts/07_R_plot.R
```

---

## 📊 Results

Results will be saved in the `results/` folder:

- FastQC HTML report  
- Trimmed FASTQ  
- Sorted BAM + index  
- VCF (variants)  
- CSV table of variants  
- Mutation plot  

---

## 📘 License

Free for learning and research use.

---

## 👨‍💻 Author

Your Name  
GitHub: https://github.com/yourusername
