README file for R package supporting the paper "EnImpute: imputing dropout events in single cell RNA sequencing data via ensemble learning".


Contents of this archive
------------------------
(1) pkg: subdirectory that contains the R package.
(2) down_sampling_experiments: subdirectory that contains scripts for performing down-sampling experiments.
(3) shiny: subdirectory that contains the Shiny application.
(4) EnImpute-manual.pdf: reference manual.


The EnImpute package has the following R-package dependencies: DrImpute, Rmagic, rsvd, SAVER, Seurat, scImpute, scRMD and stats. The dependencies will be automatically installed along with EnImpute. If the dependencies are not installed correctly, please install them by yourself. You can install the dependencies using the following commands:

# DrImpute (https://github.com/ikwak2/DrImpute)
install.packages("DrImpute")

# Rmagic (https://github.com/KrishnaswamyLab/MAGIC)
install.packages("Rmagic")

# rsvd (https://cran.r-project.org/web/packages/rsvd/index.html)
install.packages("rsvd")

# SAVER (https://github.com/mohuangx/SAVER)
library(devtools)
devtools::install_github("mohuangx/SAVER")

# Seurat (https://cran.r-project.org/web/packages/Seurat/index.html)
install.packages("Seurat")

# scImpute (https://github.com/Vivianstats/scImpute)
library(devtools)
install_github("Vivianstats/scImpute")

# scRMD (https://github.com/ChongC1990/scRMD)
library(devtools)           
devtools::install_github("ChongC1990/scRMD")

# stats (https://stat.ethz.ch/R-manual/R-devel/library/stats/html/stats-package.html)
install.packages("stats")

EnImpute also depends on the following two Python packages: dca (https://github.com/theislab/dca) and MAGIC (https://github.com/KrishnaswamyLab/MAGIC). Before installing EnImpute,  please install the two Python packages following the corresponding readme files, and check whether they can be run from the command line.

You can use the following commands to install EnImpute from GitHub.

# Step 1. Install the devtools package. Invoke R and then type
    
install.packages("devtools")

# Step 2. Load the devtools package.
    
library("devtools")

# Step 3. Install the EnImpute package from GitHub.
    
install_github("Zhangxf-ccnu/EnImpute", subdir="pkg")


Useage
Load the library EnImpute in R console, by running
library("EnImpute") 

Simply run the function EnImpute on your favorite datasets. Take the baron dataset as an example,
data("baron")
baron_imputation_result = EnImpute(baron$count.samp)

For detialed usages, please refer to "EnImpute-manual.pdf". For more examples about real data applications, please refer to the file "down_sampling_analysis.R", which performs the down-sampling experiments in the papar in the subdirectory "down_sampling_experiments".

Please do not hesitate to contact Dr. Xiao-Fei Zhang at zhangxf@mail.ccnu.edu.cn to  seek any clarifications regarding any contents or operation of the archive.