## Analysis of an individual's participation and contributions to open source and factors affecting them. 
The Github Survey Data 2017 consisits of questions and responses asked to a particular user regarding open source contributions
and participations. The survey responses are in a csv file format with 93 variables and user responses from 6029 people.
Here, I have made an attempt to analyse and understand factors affecting an individual's contribution to open source and learn some ways to analyse given. This 
analysis had been done using R.

#### Shape of Data 
Firstly, in order to understand the nature of data, the csv file was loaded into R and number of rows and columns were found.
Further, head() command was used to see the first few rows and get an idea about various attributes.

```R
df <- read.csv("/home/reen/Downloads/data_for_public_release/data_for_public_release/survey_data.csv",header = TRUE,na.strings=" ",sep = ",")
#dataframe df, header=True implies that the first row of the csv file is to be taken as header for various columns.
rows<-nrow(df) #number of rows
cols<-ncol(df) #number of columns
head(df) #outputs the first 6 rows of data and all columns(attributes) associated with it
```

#### Distribution of participants categorized by gender


![alt text](https://github.com/avneet14027/New/blob/master/Rplot_Par_gend_2.png)
