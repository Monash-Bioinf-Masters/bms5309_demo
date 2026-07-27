Here is a short exemplar outlining how to write and structure a document about a bioinformatics pipeline for RNA-sequencing analysis.

You must clearly indicate which elements of the report are code:

For simple Bash commands, write them as you executed them:
```bash
# Example bash command
samtools view -h file.bam | head -20

```markdown
## Alignment Step

Here's how to run the alignment:

```bash
# Align reads using STAR
STAR --genomeDir $GENOME_INDEX \
     --readFilesIn sample_R1.fastq sample_R2.fastq \
     --outFileNamePrefix ./aligned/
