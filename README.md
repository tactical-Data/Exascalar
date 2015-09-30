# Exascalar

This repository contains code and data for the June 2015 Exascalar analysis of the Top500 and Green500 Supercomputer lists.  

##Data  
The raw Top500 and Green500 lists, stored as .csv files. are contained in the the directories _top500data_ and _green500data_, respectively. The data are uncleaned and are as downloaded from the sites of the respective lists. They are stored here solely for convenience.   
The directory _results_ contains all the cleaned data. It contains three kinds of files:   
1. __MmmYY.csv__ is a summarized format containing the fields:  date, Exarank, exascalar, green500rank, top500rank, rmax (performance in mflops), power (in kW), mflopswatt (megaflops per watt), and the computer name. These files extend back to 2009.  
2. __MmmYY\_merged.csv__ are the merged Top500 and Green500 lists for the respective month and year. The columns of these data frames are not consistent year upon year and need to be treated specially when used to compare between years.   
3. __BigExascalar__  is a merged list of the MmmYY.csv files.  

##Programs  
__Exasclar\_Cleaner.R__ is a data cleaning program. It reads files from the raw data directories and stores them in the _results_ directory. Especially for the older lists, data cleaning is a very "hand-crafted" process.  
__Exascalar VIsualization June 2015 Rev3.Rmd__ is the analysis program. It reads files directly from teh github repository and creates the output published on [RPubs](http://rpubs.com/ww44ss/114893)  