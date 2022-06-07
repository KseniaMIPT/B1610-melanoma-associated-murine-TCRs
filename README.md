# Additional materials to the thesis project

This page contains information about B16F10 melanoma-associated murine TCRs identified by TCRgrapher following the pipeline described in the thesis.

## Frequency distribution

The folder 'Frequency distribution' contains plots showing distribution of cluster frequency among experimental groups. Every dit correspond to one mouse. Mice from the replicas are present as one boxplot. Clusters were formed by TCRs identified as significant. All clusters had frequency more than 0.25%. Visualisation were made using 'ggplot' R package.

## Motifs
 
The folder 'motifs' contains motifs for all significant clusters with frequency above the threshold. Logo was made by 'ggseqlogo' R package.

File 'Motifs (peptides with 2 groups).pdf' contains tables with comparison of motifs of Th clusters with two experimental groups identified as significant. All clusters had frequency more than 0.25%. p5, p20 and p30 showed strong immune response with a lot of intersections between clusters. Matched clusters highlighted by green. For p17 and p48 one out of two experimental groups showed poor response. However, the most abundant clusters in the groups are the same for both peptides.

## Clonotypes

Table 'clonotypes.tsv' contains information about clonotypes that form significant clusters. There are following columns:

* Read.count -- number of UMI
* frequency -- clonotype frequency in full unnormalised sample
* cdr3nt -- CDR3 nucleotide frequency
* cdr3aa -- CDR3 amino acid frequency
* bestVGene -- V gene on which the sequence was aligned
* bestDGene -- D gene on which the sequence was aligned
* bestJGene -- J gene on which the sequence was aligned
* VEnd, DStart, DEnd, JStart
* file -- the name of the source file included in the analysis. The name contains the number of the mouse
* D -- number of neighbours with the same VJ combination. A neighbour is a sequence that differs by no more than one amino acid substitution. 
* VJ_n_total -- number of sequences with the same VJ combination in the sample 
* Pgen -- generation probability of the sequence
*Pgen_sum -- sum of generation probabilities of all possible neighbours (preliminary result required for further calculations)
*Pgen_sum_corr -- corrected sum of generation probabilities of all possible neighbours 
*Pgen_by_VJ -- сonditional probability. Sum of probabilities to be generated with given VJ combination
*p_val -- p-value under null hypothesis that number of sequence's neighbours is not more than in the random model
*p_adjust -- p-value with multiple testing correction
*cluster_id -- unique number for every connected part of the graph regardless VJ combination 
*intersections -- names of files in which that sequence also occurred. Title includes peptide number and T cell subset. 
*cluster_VJ -- combination of cluster_id, V and J genes
*cluster_total_freq -- sum of frequency of all clonotypes from the cluster
*peptide -- peptide id
*type -- T cell subset
*replica