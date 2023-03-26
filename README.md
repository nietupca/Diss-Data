# Diss-Data
# 
# SOURCE PUBLICATION:
# Zhao Z, Chen L, Cao M, Chen T et al. Comparison of lncRNA Expression in the Uterus between Periods of Embryo Implantation and Labor in Mice. Animals (Basel) 2022 Feb 8;12(3). PMID: 35158722
#
# GEO Series GSE195795
#
# OVERALL DESIGN
# Pregnant 8 weeks old ICR mice at E0.5, E4.5, E15.5, and E18.5 (n=3/E) were used for a RNA-seq-based analysis of mRNA and lncRNA expression
#
# DATA PROCESSING
# Illumina Casava1.7 software used for basecalling.
# Sequenced reads were trimmed for adaptor sequence, and masked for low-complexity or low-quality sequence, then mapped to mm8 whole genome using bowtie v0.12.2 with parameters -q -p 4 -e 100 -y -a -m 10 --best --strata
# Reads Per Kilobase of exon per Megabase of library size (FPKM) were calculated using a protocol from Chepelev et al., Nucleic Acids Research, 2009. In short, exons from all isoforms of a gene were merged to create one meta-transcript. The number of reads falling in the exons of this meta-transcript were counted and normalized by the size of the meta-transcript and by the size of the library.
# Data filtering steps.Prior to assembly, the low quality reads(1,reads containing sequencing adaptors; 2,reads containing sequencing primer;3, nucleotide with q quality score lower than 20 )were removed .software CutAdapter,parameters -o 5 -p 100
# Read alignment software,software HISAT ,version 2.0 ,parameters -l fr-firststrand -mi 20 -mx 500000 -p 2 -b dta -q phred33-quals -x 9
# perform expression level for mRNAs and lncRNAs by calculating FPKM.stimate the expression levels of all transcripts.software StringTie ,version 1.3.0,parameters -b dta -q phred33-quals.
# Genome_build: mm10
# Supplementary_files_format_and_content: tab-delimited text files include FPKM values for each Sample
#
#
