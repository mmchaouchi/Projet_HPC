# Projet_HPC

# ATAC-seq workflow.
## Mohamed Malek CHAOUCHI, Babacar NDAO, Sara MOUSSADEQ
## Université Clermont auvergne, 2021

### Dependencies, in order of use:

-Initial Quality Control : 

FastQC                                 --> atac_qc_init.slurm


-Trimming : 

Trimmomotic                            --> atac_trim.slutm

                              
-Post Trimming Quality Control :

FastQC                                 --> atac_qc_post.slurm

                              
-Generating MultiQC Report : 

MultiQC                                --> multiqc.sh

                           
                              
-Sequence Alignment : 

Bowtie2                                --> atac_bowtie2.slurm

                            
                              
-Cleaning alignments by removing duplicates : 

Picard(MarkDuplicates)                 --> pikard.sh

                            
                            
-Cleaning alignments by correcting gc biases : 

deepTools(computeGCBias/correctGCBias) --> GC_Remove.sh

                
                              
-Data Exploration : 

deepTools(multiBamSummary)             --> deeptools.sh

deepTools(plotCorrelation)             --> Deeptools_Correlation.sh

deepTools(plotCoverage)                --> Deeptools_Coverage.sh

                  
-Identification of dna accessibility sites : 

MACS2(callpeak)                        --> macs2.sh

                   
                              
-Commun and unique : 

bedtools                               --> bedtools.sh

               
                              
-Get cluster usage information :

Slurm(sacct)                           --> sacct.sh


### Workflow file : workflow.sh 

### Launching workflow:
- Execute workflow.sh in main directory.
- All output will be found in "$HOME"/results/atacseq.
