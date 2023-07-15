sageQuality control for FastQ reads is an essential step in analyzing next-generation sequencing (NGS) data. It helps ensure that the sequencing data is of high quality and reliable for downstream analysis. Here are some common quality control steps for FastQ reads: 
    
1. Check sequencing quality scores: FastQ files contain quality scores for each base in the sequence. The most commonly used quality score format is Phred scores, which represent the error probability of a base call. Tools like FastQC or NGS-QC Generator can assess the quality scores and generate quality reports.   

2. Evaluate sequence length distribution: Check the length distribution of the reads in your FastQ files. Sequencing errors or adapter contamination can lead to shorter or longer reads. Tools like FastQC can provide information about read length distribution and identify any anomalies.  

3. Assess per-base sequence quality: Examine the quality scores at each position in the sequence. Low-quality bases at the ends or throughout the read may indicate sequencing errors or other issues. Tools like FastQC or PRINSEQ can generate per-base quality score plots and statistics.

4. Trim adapters and low-quality bases: If you find adapter contamination or low-quality bases in your reads, you may need to trim them. Tools like Trimmomatic, Cutadapt, or Trim Galore can remove adapters and low-quality bases, improving the overall data quality.

5. Filter out low-quality reads: Based on quality scores, you can filter out reads that do not meet certain quality thresholds. This ensures that only high-quality reads are used in downstream analyses. Tools like Trimmomatic, Cutadapt, or Fastp can perform read filtering based on quality. 

6. Analyze sequence duplication levels: High duplication levels can indicate PCR bias or other technical artifacts. Tools like FastQC or Picard MarkDuplicates can estimate sequence duplication levels and flag potentially problematic reads. 

7. Check for over-represented sequences: Identify and remove over-represented sequences that may indicate contamination or other technical issues. FastQC and PRINSEQ can detect such sequences and help with their removal. 
 
8. Validate with reference genomes: If you have a reference genome, you can align your reads to it using tools like Bowtie2, BWA, or STAR. This alignment can provide insights into mapping rates, coverage, and potential biases in your data. 

It's important to note that the specific quality control steps and tools used may vary depending on the nature of the sequencing experiment, the sequencing platform, and the specific analysis goals. It's recommended to consult the documentation of the tools you choose to use and adapt the quality control pipeline to your specific needs.
Usage : ~/Desktop/singlecell/SingleCellToolkit/sratoolkit.3.0.1-ubuntu64/bin/fastq-dump --split-3 SRR648671    
Use above code for split SRR to 2 fastq_1,fastq_2 .
Usage : /home/lbb-admin/Desktop/singlecell/SingleCellToolkit/fastqc_v0.11.9/fastqc -f fastq SRR648671_1.fastq SRR648671_2.fastq 
Use above code for Quality check of fastq_1,fastq_2 .
![image](https://github.com/Siamak-salimy/Bulk-RNA-seq/assets/34867846/5ad7833d-3f84-4d0b-9ee0-8823a75b84ca)
Here a sample of QC chart that imply the quality for fastq_2 file  of SRR648671 .
