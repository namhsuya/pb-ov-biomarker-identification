# OV serous carcinoma: Pine Biotech - Final Project
Identification of potential biomarkers by performing differential expression analysis on existing biomarker isoforms in ovarian cancer.

### TASK LIST
1. Extracted list of prognostically favorable genes for Ovarian Cancer from proteinatlas.
[prognostically favorable genes](https://www.proteinatlas.org/search/prognostic%3Aovarian+cancer%3BFavourable+AND+sort_by%3Aprognostic+ovarian+cancer+AND+show_columns%3Aprognostic)

2. Found total of 357 genes with prgnostic significance from the proteinatlas database.

3. Out of those 357 genes, 312 genes were found common in our gene RSEM raw counts downloaded from firebrowse.
[gene RSEM raw count](http://gdac.broadinstitute.org/runs/stddata__2016_01_28/data/OV/20160128/gdac.broadinstitute.org_OV.Merge_rnaseqv2__illuminahiseq_rnaseqv2__unc_edu__Level_3__RSEM_genes__data.Level_3.2016012800.0.0.tar.gz)

4. Clinical data was explored from firebrowse as well and patients with the following TCGA barcodes were identified for analysis. The patients chosen were in kept in the narrow age bracket of 55 to 58, to reduce phenotypic variations.

5. Following are the patient barcodes, with their age and stage denoted at the beginning of the barcode.
   - 56-TWO-TCGA-61-1910-01A-01R-1567-13
   - 55-TWO-TCGA-3P-A9WA-01A-11R-A406-31
   - 58-TWO-TCGA-24-2267-01A-01R-1568-13
   - 55-THREE-TCGA-09-0366-01A-01R-1564-13
   - 58-THREE-TCGA-24-1549-01A-01R-1566-13
   - 56-THREE-TCGA-24-1616-01A-01R-1566-13
   - 57-FOUR-TCGA-13-1410-01A-01R-1565-13
   - 58-FOUR-TCGA-59-2355-01A-01R-1569-13
   - 55-FOUR-TCGA-VG-A8LO-01A-11R-A406-31
  
6. The files uploaded are all grouped stagewise, for both gene, significant DEGs & isoforms of the signigicant DEGs
   -  Stage 2 vs Stage 3
   -  Stage 2 vs Stage 4
   -  Stage 3 vs Stage 4
  
7. First, DESeq2 is performed on all the prognostic genes for these 9 patients in the following manner:
   - All prgnostic genes
     -    Stage 2 patients vs Stage 3 patients - all prognostic genes => DESEq2 => Significant DEGs
     -    Stage 2 patients vs Stage 4 patients - all prognostic genes => DESEq2 => Significant DEGs
     -    Stage 3 patients vs Stage 4 patients - all prognostic genes => DESEq2 => Significant DEGs
   - All isoforms of the significant DEGs obtained from the previous step
     -    Stage 2 patients vs Stage 3 patients - all isoforms of DEGs => DESEq2 => Significant DEIs
     -    Stage 2 patients vs Stage 4 patients - all isoforms of DEGs => DESEq2 => Significant DEIs
     -    Stage 3 patients vs Stage 4 patients - all isoforms of DEGs => DESEq2 => Significant DEIs
        
 8. After completion of step 7.ii we are able to identify:
    - Which isoform of already available prognostically significant gene performs better, and with a stagewise relevance keeping the age as a constant bracket, i.e. withing 55 to 58
    - Hope to find age-wise relationship after performing a deeper age-wise grouped study
9.  Obstructions/Limitations faced
    - Stage 1 has only one datapoint with gene expression raw_count data_
    - There are no NORMAL/CONTROL types ('-01R-', '-01B-', '-01C-', '-02A-', '-01A-')
	
# HELP
Try to go through T1, and T2 on the edu-platform for in-depth understanding
