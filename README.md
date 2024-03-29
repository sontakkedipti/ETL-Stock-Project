# Introduction
                                                                        
This project was picked with the intention of utilizing stock recommendations by investingnews.com. An article that listed out six biofuel companies to invest in for 2022 was chosen as a base to work on. The biofuel companies this website suggested are Ametis, Alto Ingredients, Comstock, FutureFuel, Gevo and REX American Resources.
The idea was to scrape ticker from the paragraph titles and search for that specific ticker’s data in a folder of stock history files. The files are titled after each ticker (ex. AAPL.csv) and provides the 2021-2022 history of that stock. All data relevant to this project have been added to the resources folder for convenience of future users.
 

# Data Extraction
                                                                        
Information has been extracted from the website, transformed by adding data from csv files along with some calculations using Jupyter notebook into one cohesive data frame. Then the final dataframe was loaded to into PostgreSQL.
The database in PostgreSQL will then allow for an analyst to perform stock analysis based on the biofuel stock they saw on this website. This example could be extrapolated to any website that may present interesting stock finds or sort through a list of choice to find historical stock data the internet has to offer.


# Data Transformation

Multiple libraries of python have been used on jupyter notebook in order to transform the data. Initially data was pulled using a URL, then findings were loaded into a dataframe. The data frame then was merged onto the six csv files that were chosen for this project. The final data that appeared after merging was converted to a csv file and loaded to the database. As part of transformation the following has been achieved:

1. HTML file has been parsed to achieve the titles which generates list of stocks that were needed for this project.
2. As part of web scraping company, exchange and ticker were retrieved which was eventually mapped against 
   its stock type.
3. To maintain consistency the column names were changed lower case spelling. 
4. Extra column has been added to reflect the difference between high and low for individual dates.
5. Extra column has been added to reflect the difference between open and close for individual dates.


Flow of  steps taken for data transformation are as following:


![image](https://github.com/sontakkedipti/ETL-Stock-Project/blob/main/Code/Images/ETL%20Diagram.PNG)


# Data Loading

There were two options to chose from while deciding on a database, PostgreSQL and MONGODB. The database that was used finally for this project is PostgreSQL. As the data was consolidated into a dataframe, using a table in a database hence PostgreSQL seemed more appropriate for this project. A new database and a table was created before loading in order for PostgreSQL to receive the final data. After creating table, the final step was to load transformed data into PostgreSQL. The database is now up and running, ready for further analysis. Variables that were used to create the table are visualized as following:

![image](https://user-images.githubusercontent.com/112669805/206597495-3f059ed6-a4b4-45f6-b1d3-7518fa567b58.png)

# Conclusion

The purpose of this project was to find the most attractive biofuel stocks to invest in the year 2022. Hence necessary steps were taken to extract, transform and load the data relevant to these stocks.  This data is now ready for the next step to be analyzed further. There could be multiple targets to this future analysis like, which stock among these six can be attributed the most attractive to the niche of biofuel or are these stocks really that profitable at all or more companies can come in and out of these top six companies and so on. The same process can also be followed to prepare data for another niche segment of stocks to analyze the top most attractive stocks to trade in a specific year. The possibilities are endless from here onwards.

Regards


Sun Choi, Dipti Sontakke and Tabassum Choudhury
