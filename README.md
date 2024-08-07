This is the RNA Seq  data analysis pipeline that worked for me, using data from Stockdale et al., 2018

Basic pipeline:

1. 1. Download _1.fastq and _2.fastq of your sample from https://www.ebi.ac.uk/ena/browser/view (or however you're getting it)
  > the fastq files, if they are paired end reads like Stockdale's, they could also be labelled _forward / _reverse
2. trim reads with trimmomatic
> [https://github.com/usadellab/Trimmomatic]
3. run FASTQC analysis on your trimmed sample - checks for quality
> [https://www.bioinformatics.babraham.ac.uk/projects/fastqc/](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.11.9.zip)
4. Align fastq files with STAR
> [https://github.com/alexdobin/STAR]
5. Read your sorted.bam into R
> this is where you should be able to see your raw counts, with ensembl/gene id labels
6. Downstream analysis
