# building and Automating CEL-Seq2 pipeline

RNA sequencing has progressed remarkedly over the past few years and has become of great interest due to the ability to profile the transcriptome of organisms. Diseases or biological disorders that endanger life and health require accurate and comprehensive analysis. With RNA-Seq, the focus usually relies on gene expression, which allows studying gene expression across many samples, conditions, and diseases. 

Due to the drastically reduced costs of sequencing, RNA -Seq has become a preferred method for transcriptional analysis over microarrays4. However, challenges appeared with the standard RNA sequencing protocols due to low amounts of RNA or degraded RNA. Therefore, adaptation of single-cell RNA-Seq is of interest, which is applied in situations where the limited factor is the low amount of biological material, such as single-cell analysis. Due to the limitations with low starting amounts of RNA in single-cell and the time consuming PCR-based approach, CEL-Seq was developed for overcoming these limitations. This protocol utilizes barcoding and pooling of the samples which allows highly multiplexed analysis. Recent adaptations were made to the CEL-Seq protocol. Unique Molecular Identifiers (UMI) were integrated, enabling the reverse transcription of mRNA to be counted precisely after amplification during PCR.

Therefore this protocol was adjusted to samples of the Epigenomics facility of the UMC Utrecht. However, an automated pipeline for data analysis is lacking. Therefore this protocol was adjusted to samples of the Epigenomics facility of the UMC Utrecht. However, an automated pipeline for data analysis was lacking. Therefore, the aim is to develop a Galaxy workflow to map the RNA-seq data containing the UMIs of the CEL-Seq2 protocol. This was mediated with Galaxy tools using the galaxy training: " Understanding barcodes" and " Pre-processing of Single-Cell RNA Data". First we uploaded the data in galaxy using Filezilla, following that extracted the Unique molecular identifiers and barcodes using UMI-Tools-count, next we concatenated read2: UMI-tools extract files and mapped them to a reference genome using a gene model for annotation of the genes. Then the featurecounts was used for per-feature transcript counts, and umi-tools for per-barcode. After that we made some changes to the workflow and scripted our own tool for counting barcoded reads, mapped against references. 

Both workflows are availableble in the files: " Alternative workflow"  & " Galaxy workflow".
The script for the count matrix is availible in the file: "Script_counting_UMIBarcode"


