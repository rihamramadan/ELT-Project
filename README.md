# ELT Project Technical Report

### Extract/Data Utilized
The data was received from Kaggle. The site had YouTube data from dozens of countries but we only used csv files from Great Britian, Canada and the United States. These countries were chosen because English is the main spoken language and each country had a high use of YouTube. 


### Transformation
Once the 3 data files were extracted, the data was transformed. Multiple columns were dropped from each file so that the columns that would be used were  the only ones left. Removing extraneous data allowed for increased readability of the files. Next, each column was renamed to include an abbreviation of the country's name (i.e. 'video_id_ca and 'video_id_us). This was to ensure that when the files were merged, we can still keep track of the various columns. Lastly, an outer merge was utilized to create one file. 

### Load 
All of the data was uploaded into a non-relational database with MongoDB. The database had 4 main tables for use: 1) all countries; 2)ca_trending; 3) gb_trending; and 4) us_trending. The decision was made to have 4 tables because it allows users the option to look at all the data at once (with the use of the main table) or the user can just pull data from a country-specific table. 


