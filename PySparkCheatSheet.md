HANDS ON CHEAT SHEET
====================

Notebook Navigation
===================

| Command       | Explanation                       |
|---------------|-----------------------------------|
| shift+enter   | Run cell and move to the next one |
| ctrl+alt+P    | insert cell above                 |
| ctrl+alt+N    | insert cell below                 |
| ctrl+alt+up   | move cell up                      |
| ctrl+alt+down | move cell down                    |


Working with data frames
========================

| Command                                                       | Explanation                               |
|---------------------------------------------------------------|-------------------------------------------|
| df.printSchema()                                              | Shows the schema of the data frame        |
| df.show()                                                     | Shows the data                            |
| display(df)                                                   | Shows the data, but as nicely as possible |
| df.cache()                                                    | Puts data into memory                     |
| df.select("column_name","another_column_name")                | Selects a subset of columns               |
| df.groupBy("column_name")                                     | Groups data by a column                   |
| df.max("column_name")                                         | Maximum value in the column               |
| df.sum(“column_name”)                                         | Sum of the values in the column           |
| df.filter("column_name= 'column value to match'")             | Finds matching rows                       |
| df.withColumnRenamed(“Current Column Name",'New Column Name') | Renames columns                           |

SQL Functions – Joins
=====================

| Command                                                            | Explanation                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------|
| from pyspark.sql.functions import col                              | Imports the column handling library                                |
| df1.join(df2,col("Column Name in DF1")==col("Column Name in DF2")) | Joins two data frames based on matching columns in each data frame |

Reading and Writing Data
========================

| Command                                                                         | Explanation                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| spark.read.format('csv').options(header='false', inferSchema='true').load(path) | Reads a CSV, automatically figures out the types of columns, and sets the first row as header. |
| df.write.option("header","true").csv('path')                                    | Saves as a csv while also setting the first row as header.                                     |
