# Charleston-Data-Analytics-Cancer-Genomics-Data-Challenge
Cancer Genomics Data Challenge

One of the great challenges in treating cancer today is being able to match each cancer patient with the drug or drugs that will be most effective at treating that person’s individual cancer.  Unfortunately, two patients that have the same ‘type’ of cancer i.e. lung, breast, colon etc. often have dramatically different responses to the same drug.  Recently, advances in the field of Cancer Genomics are making it possible to better predict the best treatment for a patient by characterizing the genetic make-up of each patient’s tumor.  For some drugs, we now know what signals to look for in this genetic data in order to determine which tumors will respond to a drug and which will not.  For other drugs, these signals are not known.  
In this data challenge, you will be provided with genomic data from a group of tumors that were treated with a new cancer drug that is currently in clinical trials.  In addition to the genomic data, each tumor will be labeled with how it responded to the drug.  This data comes from two separate studies that used different response metrics to measure the tumor response so I created a Z-score column which should allow for comparison of responses across both studies.  The lower the Z-score is the more sensitive that tumor was to the drug.  

There are 255 tumors in the data set and you will see that for some of them the value of the response variable is labeled as ‘hidden’.  The challenge is to use the genomic data to develop a classifier or prediction algorithm that will allow you to rank the hidden samples in order from most sensitive to least sensitive to the drug.    

There are three genomic data sets to work with.  In each data set the first column contains a unique identifier for each individual tumor (this column can be used as a key to link all of the data sets together) while the second and third columns contain sensitivity scores and the fourth column contains the sensitivity Z-score.  The remaining columns show the measured data for each tumor for each gene in the human genome.  The data sets are: 

mutations.csv--In this data, if a gene does not contain a mutation in that tumor it will say NA.  If the gene does contain a mutation, there will be a description of the mutation that will look something like ‘I38E’ or ‘V600E’.

gene_expression.csv--In this data set there is a numeric value for each gene that indicates how active or inactive that gene is in that tumor. The higher the number the more active the gene is.  

copy_number.csv--This data shows how many copies of each gene are present in the tumor.  Values here range from -2 (meaning the gene has been deleted in this tumor) up to 2 meaning there are numerous extra copies of this gene in the tumor.  

Answer_key.csv—This file holds an answer key so you can see how your classifier performs.

If any of this doesn’t make sense just let me know.  I’m happy to clarify anything or answer any questions.
