# Homework-CIS-9440

For this project, I will be using a shooting incident data set from the NYPD dating back to 2006 through the end of the previous calendar year. Here is the link to the data set: (https://data.cityofnewyork.us/Public-Safety/NYPD-Shooting-Incident-Data-Historic-/833y-fsy8/about_data). It contains 20 columns and 28500 rows. 

For my data source, I used NYC open data to find this dataset about shootings in NYC, which includes information of the shooting like place, time, date; age group, sex, and race of the victim and perpertrator.

Firstly I used a WebAPI script to extract the data from the site and then open it to take quick look at the data. Shortly after, I saved the extracted data in a csv file. 
Next step, I decided to store the data in an Azure blob storage. Afterwards I created a data model with the data dictionary provided to me by the site. Granted the data model at this point is just a rough draft. 
After creating the data model, I used Jupyter notebook to read the data in the Azure blob where my data was sitting to clean it and later transform it. I started by dropping all the null and NaN values and leaving those cells blank because 
I downloaded the CSV and checked to see that theres a lot of missing data but opening it in jupyter notebook created a lot of placeholders which I didn't need. Therefore, I removed null and Nan values and some of the columns like 
x and y coordinates which were not needed as it's oddly specific and made analysis of the data more complicated considering the amount of rows. Later, I transformed the data by reformating and slicing the date attributees into Year, Quarter, 
Month, Week, Day, Day of the week. After that I created dimension tables and facts tables with respect to data model which i needed to update because of the extra data attributes. After that I loaded the data into PostgreSQL.

