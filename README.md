# OV serous carcinoma: Pine Biotech - Final Project
Identification of potential biomarkers by performing differential expression analysis on existing biomarker isoforms in ovarian cancer.

# DONE
	A. gene-isoform mapping
	B. expression raw_count data:
		1. gene raw_count data collected from firebrowse
		2. isoform raw_count data collected from firebrowse
	C. normalization
		1. gene raw_count data quantile normalized + log transformed (QN_LT) on server.t-bio.info 
		[geneFile](https://github.com/namhsuya/pb-ov-biomarker-identification/blob/master/not_normalized/REQUIRED_stagewise_allGenesRSEM_extracted.txt)
		2. isform raw_count data quantile normalized + log transformed (QN_LT) on server.t-bio.info 
		[isoformFile](https://github.com/namhsuya/pb-ov-biomarker-identification/blob/master/not_normalized/REQUIRED_stagewise_allisoformsRSEM_extracted.txt)

# TO BE DONE
	1. Filter out desired biomarkers (as sent by Chitta sir) from QN_LT file for _(DeSeq2/edgeR)_
	2. Map genes to their corresponding isoforms on the (isoformFile)
	3. Stage-wise segregation (5 samples each from Stage 1 to 4, and 5 from normaltype)
	   _IMP: i. Stage 1 has only one datapoint with gene expression raw_count data_
	   	ii. There are no NORMAL/CONTROL types ('-01R-', '-01B-', '-01C-', '-02A-', '-01A-')
	4. Perform DeSeq2/edgeR of stagewise pairs to try to identify stage-specific DEGs
	
# HELP
	Try to go through T1, and T2 on the edu-platform for in-depth understanding
