# GPH-2338-final-assignment

## Data Sources

### HSQ_J, DBQ_J, DUQ_J, DPQ_J, SMQ_J Datasets

https://wwwn.cdc.gov/nchs/nhanes/Search/DataPage.aspx?Component=Questionnaire&CycleBeginYear=2017

### OHXDEN Oral Health Dataset

https://wwwn.cdc.gov/nchs/nhanes/Search/DataPage.aspx?Component=Examination&CycleBeginYear=2017

## Installing Datasets:
##first set working directory to download directory then install via xport

setwd("/Users/charliewhite/Downloads")
DPQ_J <- read.xport("DPQ_J.XPT.txt")
OHXDEN <- read.xport("OHXDEN_J.XPT.txt")
SMQ_J <- read.xport("SMQ_J.XPT.txt")
DBQ_J <- read.xport("DBQ_J.XPT.txt")
HSQ_J <- read.xport("HSQ_J.XPT.txt")
DUQ_J <- read.xport("DUQ_J.XPT.txt")

## Data Cleaning and Pre-processing Steps
unused columns dropped 
combine drug use variable
drop missing values 
# a value of 0 indicates person has not smoked at least 100 cigarettes in their lifetime
# a value of 1 indicates they have smoked at least 100 cigarettes in their lifetime
# assigning a 1 to teeth that required medical attention and a 0 to sound permanent/primary teeth
# assigning a 1 to sound permanent/primary teeth and a 0 to implants/missing teeth

datasets then combined

#creating DPQ_score from mental health questionnaire (DPQ010 + df$DPQ020 + df$DPQ030 + df$DPQ040 + df$DPQ050 + df$DPQ060 + df$DPQ070 + df$DPQ080 + df$DPQ090 + df$DPQ100)
#creating number of healthy permanent teeth variable (df$OHX01TC + df$OHX02TC + df$OHX03TC + df$OHX04TC + df$OHX05TC + df$OHX06TC + df$OHX07TC + df$OHX08TC +  df$OHX09TC + df$OHX10TC + df$OHX11TC + df$OHX12TC +  df$OHX13TC + df$OHX14TC + df$OHX15TC + df$OHX16TC +  df$OHX17TC + df$OHX18TC + df$OHX19TC + df$OHX20TC +  df$OHX21TC + df$OHX22TC + df$OHX23TC + df$OHX24TC +  df$OHX25TC + df$OHX26TC + df$OHX27TC + df$OHX28TC + df$OHX29TC + df$OHX30TC + df$OHX31TC + df$OHX32TC)
#creating number of caries variable (df$OHX02CTC + df$OHX03CTC + df$OHX04CTC + df$OHX05CTC + df$OHX06CTC + df$OHX07CTC + df$OHX08CTC + df$OHX09CTC + df$OHX10CTC + df$OHX11CTC + df$OHX12CTC + df$OHX13CTC + df$OHX14CTC + df$OHX15CTC + df$OHX18CTC + df$OHX19CTC + df$OHX20CTC + df$OHX21CTC + df$OHX22CTC + df$OHX23CTC + df$OHX24CTC + df$OHX25CTC + df$OHX26CTC + df$OHX27CTC + df$OHX28CTC + df$OHX29CTC + df$OHX30CTC + df$OHX31CTC)

# split data into test and training sets
#decision tree created
## Linear, Lasso, and Ridge Regression created
## Generating Binary DEP Variable with 8 as the midline
## Logistic Regression, LDA, QDA, KNN






  


