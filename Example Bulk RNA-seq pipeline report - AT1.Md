# Example RNA-sequencing Pipeline Report

Here is a short exemplar outlining how to write and structure a document about a bioinformatics pipeline for RNA-sequencing analysis.

## Summary/Overview

*Begin with a brief description of your pipeline, its main steps, inputs and what it produces*

This report describes a bioinformatics pipeline for analysing bulk RNA-sequencing from 4 samples of murine T-cells, two from black mice and two from white mice. Starting with raw FastQ files, it performs data QC and adapter trimming, aligns reads to the mouse reference genome, obtains transcript counts and verifies sample identity with a PCA plot. 

## Input Data

*List the input files used by your pipeline in this analysis. I've chosen to use a table*

| Sample Name | FastQ files |
|----------|----------| 
| BlackMouse_1 | BM1_R1.fastq.gz, BM1_R2.fastq.gz | 
| BlackMouse_2 | BM2_R1.fastq.gz, BM2_R2.fastq.gz |
| WhiteMouse_1 | WM1_R1.fastq.gz, WM1_R2.fastq.gz |
| WhiteMouse_2 | WM2_R1.fastq.gz, WM2_R2.fastq.gz |

## Pipeline Implementation

*Describe each step in your pipeline, its inputs, outputs and parameters. The intention is to make it possible for others (i.e., your lecturers) to reproduce the same results you got.*

*Numbered sub-headings will add clarity and structure to your report.

### 1. Quality Control

*Briefly describe the purpose and aim of this stage of the pipeline. Provide software used and version*

Read quality was assessed using FastQC (version v0.12.1) to detect presence of possible sequence artefacts

*You must clearly indicate which elements of the report are code by using distinct code blocks. Each block should have an accompanying description.*

Create a new directory for FastQC output.

___For Bash commands, write them as you executed them:___
```bash
mkdir -p fastqc_output
``` 

___For bioinformatics tools, provide the command with all inputs and parameters used:___

### 2. Adapter Trimming

### 3. Read alignment

Read alignment was performed with STAR read aligner.

*This is NOT the aligner you will be using. STAR shown for illustration purposes only.*

```markdown

Here's how to run the alignment:
# Align reads using STAR
STAR --genomeDir $GENOME_INDEX \
     --readFilesIn WM1_R1.fastq.gz WM1_R2.fastq.gz \
     --outFileNamePrefix ./aligned/
```

