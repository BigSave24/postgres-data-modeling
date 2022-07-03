# postgres-data-modeling

Define fact and dimension tables for a star schema and write an ETL pipeline that transfers data from files in two local directories into Postgres database.

Do the following steps in your README.md file.

Discuss the purpose of this database in the context of the startup, Sparkify, and their analytical goals.
How to run the Python scripts
An explanation of the files in the repository
State and justify your database schema design and ETL pipeline.
[Optional] Provide example queries and results for song play analysis.

Here's a https://www.markdownguide.org/basic-syntax/guide on Markdown Syntax.\*

Provide DOCSTRING statement in each function implementation to describe what each function does.

## Data Modeling with Postgres

Data modeling using a Postgres database using an optimized design for querying against song play analysis

## Summary

This data engineering project focuses on developing fact and dimension tables for a Postgres database star schema. The database will be used to query song play data for further analysis. A ETL (Extract, Transform, Load) pipeline is created using Python, Pandas, JSON, and SQL. The pipeline injests JSON formatted log files which is then prepared, filtered, and inserted into the database tables.

Context: A fictional company, Sparkify, is collecting song and user activity data from their music streaming app. Their analytics team wants to have a way to query the collected data for further analysis. Currently, the data is collected seperately (user activity, songs) as raw data in JSON format. The ETL pipeline will ingest the log files from its location and convert them into tables for a Postgres database.

The final database schema will ba a star design, one fact table and multiple dimension tables:

`Fact`

- `songplays` records in log data associated with songplays

`Dimension`

- `users` users in the app
- `songs` songs in the music database
- `artists` artists in the music database
- `time` timestamps of records in the songplays in specific units

## Requirements

---

The following software is needed to run this project:

- [Python 3](https://www.python.org/downloads/)
- [Pandas](https://pandas.pydata.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [JSON](https://www.json.org/json-en.html)
- [Jupyter](https://jupyter.org/)
- [Psycopg](https://www.psycopg.org/docs/)
- [Python os Library](https://docs.python.org/3/library/os.html)
- [Python glob Library](https://docs.python.org/3/library/glob.html)

## Running the Postgres Data Modeling ETL Pipeline

---

### Project Files

- `data folder` Location for stored log files
- `create_tables.py` Python code functions to create database and create/drop tables
- `etl.ipynb` ETL notebook file to build and test pipeline
- `etl.py` Main ETL pipeline file
- `sql_queries.py` Python code parameters to create tables, insert and query database data
- `test.ipyb` Test notebook file to test pipeline run and database data
- `README.md` README documentation

### Open a terminal window in project directory

Linux\Mac - Use the default terminal application.
Windows - You can use a terminal application such as
[Git Bash](https://gitforwindows.org/) or [Ubuntu](https://www.howtogeek.com/265900/everything-you-can-do-with-windows-10s-new-bash-shell/).

### Create database and tables

##### COMMAND: `python create_tables.py`

### Run ETL pipeline

##### COMMAND: `python etl.py`
