# Example RNA-sequencing Pipeline Report

Here is a short exemplar outlining how to write and structure a document about a bioinformatics pipeline for RNA-sequencing analysis.

## Summary/Overview

*Begin with a brief description of your pipeline, its primary functions, inputs and outputs*

This report describes a bioinformatics pipeline for analysing bulk RNA-sequencing from 4 samples of murine T-cells, two from black mice and two from white mice. Starting raw FastQ files, it performs 

## Input Data

*List the input files used by your pipeline in this analysis. I've chosen to use a table*

| Sample Name | FastQ files |
|----------|----------| 
| BlackMouse_1 | BM1_R1.fastq.gz, BM1_R2.fastq.gz | 
| BlackMouse_2 | BM2_R1.fastq.gz, BM2_R2.fastq.gz |
| WhiteMouse_1 | WM1_R1.fastq.gz, WM1_R2.fastq.gz |
| WhiteMouse_2 | WM2_R1.fastq.gz, WM2_R2.fastq.gz |

## Pipeline Functionality

*Describe each step in your pipeline, its inputs, outputs and parameters*

*You must clearly indicate which elements of the report are code by using distinct code blocks. Each block should have an accompanying description.*

*Numbered sub-headings will add clarity and structure to your report.

### 1. Quality Control

Create a new directory for FastQC output.

```bash
# For simple Bash commands, write them as you executed them:
mkdir -p fastqc_output
``` 



```markdown
## Alignment Step

Here's how to run the alignment:
# Align reads using STAR
STAR --genomeDir $GENOME_INDEX \
     --readFilesIn WM1_R1.fastq.gz WM1_R2.fastq.gz \
     --outFileNamePrefix ./aligned/
