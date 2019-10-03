# OV serous carcinoma: Pine Biotech - Final Project
Identification of potential biomarkers by performing differential expression analysis on existing biomarker isoforms in ovarian cancer.

### TASK LIST
- [x] Gene-isoform mapping [map](https://github.com/namhsuya/pb-ov-biomarker-identification/blob/master/gene_isoform_mapping/gene_isoform_mapped.txt)
- [x] Expression raw_count data
  - [x] gene raw_count data collected from firebrowse
  - [x] isoform raw_count data collected from firebrowse
- [x] Normalization
  - [normalized gene rsem](https://github.com/namhsuya/pb-ov-biomarker-identification/blob/master/normalized/ov_stagewise_all_geneRSEM_QN5_LT_REQUIRED_stagewise_allgeneRSEM_extracted_Threshold_5_normalized.txt)
  - [normalized isoform rsem](https://github.com/namhsuya/pb-ov-biomarker-identification/blob/master/normalized/ov_stagewise_all_isoformRSEM_QN5_LT_REQUIRED_stagewise_allisoformRSEM_extracted_Threshold_5_normalized.txt)
 - [x] Perform gene raw_count data quantile normalization(5) + log transformation
 - [x] Perform isform raw_count data quantile normalization(5) + log transformation
- [ ] Filter out desired [biomarkers](https://github.com/namhsuya/pb-ov-biomarker-identification/blob/master/existing_OV_biomarker.txt) (as sent by Chitta sir) to find DEGs
- [ ] Map genes to their corresponding isoforms on the (isoformFile)
- [ ] Stage-wise segregation (5 samples each from Stage 1 to 4, and 5 from normaltype)
  - Stage 1 has only one datapoint with gene expression raw_count data_
  - There are no NORMAL/CONTROL types ('-01R-', '-01B-', '-01C-', '-02A-', '-01A-')
- [ ] Perfor DESeq2 for isoforms of selected biomarkers to study their clinical significance  
- [ ] \(OPTIONAL)Perform Unsupervised analysis to find out stage dependency of the selected biomarkers
	
# HELP
Try to go through T1, and T2 on the edu-platform for in-depth understanding
