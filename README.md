REPORT ON 10 DAYS NGS WORKSHOP.
WHAT IS NGS ?
Next-Generation Sequencing (NGS) is a high-throughput, massively parallel sequencing technology that allows for the simultaneous sequencing of millions of DNA fragments. It determines the precise order of nucleotides (A,T,C,G) much faster and cheaper than traditional Sanger sequencing.

All the work was done using Galaxy an open source, web-based platform for data intensive biomedical research. For data download we used https://zenodo.org/records/4249555 We used Raw mouse mammary RNA-Seq data (fastq), uploaded the 4 files on galaxy and used certain tools- 
<img width="1020" height="307" alt="image" src="https://github.com/user-attachments/assets/1f2558e9-2d88-4c16-9492-906a9d8a7efb" /> 
1. FASTQC TOOL
Think of FastQC as the "Report Card" for your sequencing run. Before you do any actual analysis (like finding mutations or assembling a genome), you must run this tool to see if your data is "clean" or "garbage."
<img width="1012" height="693" alt="image" src="https://github.com/user-attachments/assets/2fa077ea-0e9c-48fd-a3b7-bfae417ff99f" />
2. TRIM GALORE
Trim Galore is a Perl-based wrapper script used in bioinformatics to automate the quality control and trimming of High-Throughput Sequencing NGS) data. It integrates the functionality of Cutadapt (for removing adapters and low-quality bases) and FastQC (for post-trimming quality checks) into a single, streamlined workflow.
<img width="1003" height="715" alt="539628333-fa18c1ee-dc7e-4332-8456-d6f1c8f38e01" src="https://github.com/user-attachments/assets/6e0aac9f-5c91-46b3-b7d9-6ab4c58b2947" />
3. BOWTIE2
After you have cleaned your data with Trim Galore, you have millions of short DNA fragments (reads). Now, you need to figure out where exactly in the genome each fragment came from. Bowtie2 does this job.
<img width="1010" height="724" alt="image" src="https://github.com/user-attachments/assets/f56c9b62-a57d-4b22-9e36-b8a2778791f6" />
4. . FEATURECOUNTS
FeatureCounts is the tool you use for Quantification (Counting). You have already aligned your reads to the genome using Bowtie2, but knowing where the reads are isn't enough. You need to know how many reads landed on Gene A versus Gene B. This tells you if a gene is highly expressed (active) or not.
<img width="1008" height="690" alt="image" src="https://github.com/user-attachments/assets/fc5acf66-97d3-4748-b270-c95504b04c92" />
5.DEseq2 DESeq2 is the final and most critical step in your RNA-Seq pipeline. It is the tool that performs Differential Gene Expression (DGE) analysis.
<img width="1019" height="717" alt="image" src="https://github.com/user-attachments/assets/7743ab17-fd31-47da-8914-b1a8153b5c65" /><img width="995" height="727" alt="539629678-7ddb003b-5b52-4135-bf26-49879785f566" src="https://github.com/user-attachments/assets/2d30faf9-a404-45d8-910f-324d0ac9938b" />
<img width="1015" height="717" alt="539629760-e3b2fc44-e980-48db-92dd-25c084f34ce0" src="https://github.com/user-attachments/assets/ff514502-fee1-42e8-b786-eb15bb38062b" />
6. HEATMAP2
heatmap.2 is the specific R function (from the package gplots) used to create the most colorful and informative graph in your RNA-Seq project: the Heatmap.
<img width="1012" height="664" alt="539630075-e4aa0c87-f588-469b-9bb1-d45b1cbcf9ee" src="https://github.com/user-attachments/assets/56920000-2122-4ce9-8a25-d3daa0a6aee6" />
7. KYOTO ENCYCLOPEDIA OF GENES AND GENOME (KEGG) KEGG stands for the Kyoto Encyclopedia of Genes and Genomes. After you finish your DESeq2 analysis and Heatmap, you have a list of important genes. But a list of names (e.g., "PFK1, HK2, LDHA") is boring and hard to understand. KEGG is the tool that puts those genes onto a "Map" to show you how they work together.
<img width="1030" height="734" alt="539630287-b866f0a0-120e-44e6-8dd8-e0539fb389a4" src="https://github.com/user-attachments/assets/66ed207a-271b-4751-8988-6c1da0f96478" />
