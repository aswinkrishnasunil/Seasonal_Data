# Seasonal_Data
python tabula pdf table fetching codes

## README

This repository contains code to read and extract tables from a PDF file and write them to a SQLite database.

To use the code, you will need to install the following Python libraries:

* tabula
* sqlalchemy

Once you have installed the required libraries, you can run the code with the following command:

python
python main.py


This will create a SQLite database called `db_seasonal.db` and populate it with the tables from the PDF file.

The tables in the database can be accessed using the SQLAlchemy engine object. For example, the following code will print the contents of the `table1` table:

python
import sqlalchemy

engine = sqlalchemy.create_engine('sqlite:///db_seasonal.db')

with engine.connect() as conn:
    result = conn.execute('SELECT * FROM table1')

for row in result:
    print(row)


You can also use the SQLAlchemy engine object to write new data to the database or update existing data.

## Usage example

To use the code to read and extract tables from a PDF file and write them to a SQLite database, follow these steps:

1. Clone this repository to your local machine.
2. Install the required Python libraries:
    * tabula
    * sqlalchemy
3. Open a terminal and navigate to the directory where you cloned the repository.
4. Run the following command to read the PDF file and extract the tables:

python
python main.py


5. This will create a SQLite database called `db_seasonal.db` and populate it with the tables from the PDF file.
6. You can then access the tables in the database using the SQLAlchemy engine object.

For example, the following code will print the contents of the `table1` table:

python
import sqlalchemy

engine = sqlalchemy.create_engine('sqlite:///db_seasonal.db')

with engine.connect() as conn:
    result = conn.execute('SELECT * FROM table1')

for row in result:
    print(row)


You can also use the SQLAlchemy engine object to write new data to the database or update existing data.
