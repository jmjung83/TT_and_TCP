## [Publication Title]
## Characterizing therapeutic signatures of transcription factors in cancer by incorporating profiles in compound treated cells (by Jinmyung Jung)

## [Environment]
* python 3.7.6
* pandas 1.0.3
* numpy 1.18.1
* scipy 1.4.1
* matplotlib 3.1.3
* statsmodels 0.11.0
* networkx 2.4
* gseapy 0.9.18

## [jupyter notebook files]
### << pre-proccessing >>
* preProc1 (LINCS).ipynb:
  * process compound induced gene expressions in LINCS(The Library of Integrated Network-Based Cellular Signatures)
  * The used Broad_LINCS_Level3_file can be downloaded at https://bit.ly/2ux0TZL (not available in this github repository due to large-file size (44GB))
* preProc2 (LINCS and GDSC).ipynb:
  * process compound induced cell viabilities in GDSC(Genomics of Drug Sensitivity in Cancer)
  * get common compounds between LINCS and GDSC
* preProc3 (Fold Change).ipynb:
  * get fold-changes of expressions induced by the common compounds of the two databases
* preProc4 (therapeutic effect estimation).ipynb:
  * estimate effectiveness of compound treatments and selecte cell lines by the two criteria, yielding A375 and HT29 cell lines
* preProc5 (TF activity calculation)_main.ipynb:
  * estimate TF activity based on the computed fold-changes and TF target interactions (TRUST2) by using VIPER R package (main)
* preProc5 (TF activity calculation)_viper_R_code.ipynb:
  * estimate TF activity based on the computed fold-changes and TF target interactions (TRUST2) by using VIPER R package (VIPER R code)
### << main analysis >>
* mainAnal1 (TT score and significant TTs).ipynb:
  * compute therapeutic TF (TT) scores and select a significant set of TTs with FDR 1.0e-05
* mainAnal2 (evaluation for significant TTs).ipynb:
  * hypergeometric tests for TTs with CRISPR-cas9 (essential genes), TTD (therapeutic targets), TSgene (Tumor suppressors), uniprot (oncogenes and tumor suppressors)
* mainAnal3 (TCP scores and significant TCPs).ipynb:
  * compute therapeutically correlated TF pair (TCP) scores and a significant set of TCPs with FDR 0.05
* mainAnal4 (evaluation for significant TCPs).ipynb:
  * hypergeometric tests for the proteins on the paths between TCPs with TTD (therapeutic targets), TSgene (Tumor suppressors), uniprot (oncogenes and tumor suppressors)
* mainAnal5 (visualization of results).ipynb:
  * visualization of three main results
### << discussion >>
* discussion1 (conflicting TTs).ipynb:
  * TFs having conflict TT scores between the A375 and HT29 cell lines
