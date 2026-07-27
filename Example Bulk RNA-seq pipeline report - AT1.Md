Here is a short exemplar outlining how to write and structure a document about a bioinformatics pipeline for RNA-sequencing analysis.

You must clearly indicate which elements of the report are code:

```markdown
## Alignment Step

Here's how to run the alignment:

```bash
# Align reads using STAR
STAR --genomeDir $GENOME_INDEX \
     --readFilesIn sample_R1.fastq sample_R2.fastq \
     --outFileNamePrefix ./aligned/
