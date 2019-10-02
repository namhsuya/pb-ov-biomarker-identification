# OV serous carcinoma: Pine Biotech - Final Project
Identification of potential biomarkers by performing differential expression analysis on existing biomarker isoforms in ovarian cancer.

### TASK LIST
- [x] Gene-isoform mapping
- [x] Expression raw_count data
  - [x] gene raw_count data collected from firebrowse
  - [x] isoform raw_count data collected from firebrowse
- [x] Normalization
      -[normalized gene rsem](https://github.com/namhsuya/pb-ov-biomarker-identification/blob/master/normalized/ov_stagewise_all_geneRSEM_QN5_LT_REQUIRED_stagewise_allgeneRSEM_extracted_Threshold_5_normalized.txt)
      -[normalized isoform rsem](https://github.com/namhsuya/pb-ov-biomarker-identification/blob/master/normalized/ov_stagewise_all_isoformRSEM_QN5_LT_REQUIRED_stagewise_allisoformRSEM_extracted_Threshold_5_normalized.txt)
 - [x] gene raw_count data quantile normalized + log transformed (QN_LT) on server.t-bio.info [geneFile](https://github.com/namhsuya/pb-ov-biomarker-identification/blob/master/not_normalized/REQUIRED_stagewise_allGenesRSEM_extracted.txt)
 - [x] isform raw_count data quantile normalized + log transformed (QN_LT) on server.t-bio.info [isoformFile](https://github.com/namhsuya/pb-ov-biomarker-identification/blob/master/not_normalized/REQUIRED_stagewise_allisoformsRSEM_extracted.txt)
- [ ] Filter out desired biomarkers (as sent by Chitta sir) from QN_LT file for _(DeSeq2/edgeR)_
- [ ] Map genes to their corresponding isoforms on the (isoformFile)
- [ ] Stage-wise segregation (5 samples each from Stage 1 to 4, and 5 from normaltype)
     - Stage 1 has only one datapoint with gene expression raw_count data_
     - There are no NORMAL/CONTROL types ('-01R-', '-01B-', '-01C-', '-02A-', '-01A-')
- [ ] Perform DeSeq2/edgeR of stagewise pairs to try to identify stage-specific DEGs
	
# HELP
Try to go through T1, and T2 on the edu-platform for in-depth understanding
