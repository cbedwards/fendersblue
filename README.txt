This folder contains the dat and scripts necessary to replicate analyses in Changes in phenology and abundance of an at-risk butterfly by Rachael E. Bonoan, Elizabeth Crone, Collin B. Edwards, Cheryl B. Schultz. 

You are likely to want one of the four key files:

`1_raw_data/SERDP Phenology - Fenders Blue - 1993-2019 20191203.csv` is the raw data file.
`3_scripts/Online Resource 1.Rmd` (generates Appendix S1) contains the code to load the raw data, clean it, and fit phenological curves to the cleaned data. This should run "out of the box" if you have Rstudio and the appropriate R packages. It creates...
`4_res/yearly-summary-full.csv`, which is the key results file of our analysis. This contains abundance and phenology estimates on a yearly basis for each of our sites. It is used in...
`3_scripts/Online Resource 2.Rmd` (generates Appendix S2) which looks at abundance and phenology trends through time, relationships between those measures, carries out post-hoc analyses, etc, and generates plots. This should run "out of the box" if you have Rstudio and the appropriate R packages.

Directory structure :
   1_raw_data : Raw data lives here;
      SERDP Phenology - Fenders Blue - 1993-2019 20191203.csv : Latest version of the raw fendersblue data. ;
   2_data_wrangling : Cleaned data lives here.;
      cleandat.RDS : Cleaned data - This is not much modified from the raw data - mostly handling data formats;
      dat.rds : small modification to cleandat.RDS. May be of use for diagnostics.;
      dat_good.rds : dat.rds, but wtihout some problematic years. May be of use for diagnostics.;
   3_scripts : All scripts live here. Currently active line of scripts are analysis-*.Rmd;
      Online Resource 1.Rmd : Data cleaning and estimation of abundance phenology metrics. Source code for appendix S1;
      Online Resource 2.Rmd : Analysis of phenological and abundance trends; figure making. Source code for appendix S2;
   4_res : Results live here. See internal README for details of the three results files. All results files are generated from 3_scripts/analysis-final.Rmd. Key file here is yearly-summary-full.csv ;
      sitely-summary-full.csv : abundance and phenology metrics, aggregated to site level;
      yearly-summary.csv : abundance and phenology metrics, aggregated to year-within-site level level. Fit with a separate model for each site;
	  yearly-summary-full.csv : as yearly-summary.csv, but using a single model to fit all sites at once. THIS IS THE KEY DATA FILE OF THIS ANALYSIS;
   5_figs : folder used to hold figures. Empty.
   fendersblue.Rproj : Rproject for this set of analyses. Helpful to allow R code to automatically point to the correct directory.
   README-files.txt : This document.
