I’m currently working on a project that has multiple very large CSV files (6 gigabytes+). Normally when working with CSV data, I read the data in using pandas and then start munging and analyzing the data. With files this large, reading the data into pandas directly can be difficult (or impossible) due to memory constrictions, especially if you’re working on a prosumer computer. In this post, I describe a method that will help you when working with large CSV files in python.

While it would be pretty straightforward to load the data from these CSV files into a database, there might be times when you don’t have access to a database server and/or you don’t want to go through the hassle of setting up a server.  If you are going to be working on a data set long-term, you absolutely should load that data into a database of some type (mySQL, postgreSQL, etc) but if you just need to do some quick checks / tests / analysis of the data, below is one way to get a look at the data in these large files with python, pandas and sqllite.

To get started, you’ll need to import pandas and sqlalchemy. The commands below will do that.
```
import pandas as pd
from sqlalchemy import create_engine

file = '/path/to/csv/file'

print pd.read_csv(file, nrows=5)

csv_database = create_engine('sqlite:///csv_database.db')

chunksize = 100000
i = 0
j = 1
for df in pd.read_csv(file, chunksize=chunksize, iterator=True):
      df = df.rename(columns={c: c.replace(' ', '') for c in df.columns}) 
      df.index += j
      i+=1
      df.to_sql('table', csv_database, if_exists='append')
      j = df.index[-1] + 1
      
df = pd.read_sql_query('SELECT * FROM "table"', csv_database)


```
https://pythondata.com/working-large-csv-files-python/
