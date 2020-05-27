## Instructions

1. Open PGAdmin and create a database called etl_db.
	-If state_consumption and state_renewable tables already exist drop them
2. From schema.txt run #create table state_consumption
3. From schema.txt run #create table state_renewable
4. Run etl.ipynb 
5. Run EnergyConsumption.ipynb
6. Run ToDatabase.ipynb
7. From schema.txt run #example query


## ETL Energy Consumption

The purpose of this project is to merge, transform, and load energy consumption data from multiple sources as part of the ETL project. The United States consume a large amount of energy from multiple sources. Renewable energy is important because it limits the fuel amount used regularly which causes stress on the environment. For this project, data was extracted from a series of CSV files. 

## [](https://github.com/warrenallen/covid202/blob/master/final-report-md-template.md#code-walkthrough)Code Walkthrough

![](Resources/Renewable_Energy.png)

 - Retrieved the data from the website United States Renewable Energy and downloaded it as a CSV file.
 - Then cleaned the data and created new dataframe.

![](Resources/US_Consumption.png)

 - Our first steps in cleaning up the datasets which variables were not relevant. The last step was to transfer our final output into a Database. We created a database and respective tables to match the columns from the final Panda’s Data Frame using MySQL and then connected to the database using SQLAlchemy and loaded the result.


![](Resources/toSQL_DB.png)

 - Merged the CSV files.
 - Created the database in SQL using PGadming
 - Then Appened to the database using the SQLAlchemy within Jupyter notebook.


##To Create the Database in MySQL

![](Resources/state_ERD.png)

![](Resources/SQL_queries.png)


##The link to the CSVs

- Source 1 (https://www.eia.gov/state/rankings/) is the energy rankings of states.
- Source 2 (https://data.world/doe/united-states-renewable-energy) lists the different renewable sources of energy.
- Source 3 (http://www2.census.gov/programs-surveys/popest/datasets/2010-2019/national/totals/nst-est2019-alldata.csv?# ) is a table of states and population.
