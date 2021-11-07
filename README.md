# Projet_HPC

# ATAC-seq workflow.
# Mohamed Malek CHAOUCHI, Babacar NDAO, Sara MOUSSADEQ
# Université Clermont auvergne, 2021

# Dependencies, in order of use:
# FastQC                                 --> atac_qc_init.slurm
# Trimmomotic                            --> atac_trim.slutm
# FastQC                                 --> atac_qc_post.slurm
# MultiQC                                --> multiqc.sh
# Bowtie2                                --> atac_bowtie2.slurm
# Picard(MarkDuplicates)                 --> pikard.sh
# deepTools(computeGCBias/correctGCBias) --> GC_Remove.sh
# deepTools(multiBamSummary)             --> deeptools.sh
# deepTools(plotCorrelation)             --> Deeptools_Correlation.sh
# deepTools(plotCoverage)                --> Deeptools_Coverage.sh
# MACS2(callpeak)                        --> macs2.sh
# bedtools                               --> bedtools.sh

#Workflow file : Workflow.sh --> launch full workflow
