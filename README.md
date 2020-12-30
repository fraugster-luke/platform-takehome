### Fraugster Platform Team Take-Home Challenge!
In this repo is a **docker-compose.yml** file that will launch two docker containers. One will be a fully functional PostgreSQL database container, and the other will run a python script called **insert.py**. 

There are two parts to this task:

**Task One** - Clone this repo to your local dev system. Add Python code to the **insert.py** file, and modify the other files as needed to do the following:
    
- When the "docker-compose up" command is run, the **insert.py** file will connect to the database.
- The **insert.py** file will create a new database called "accounts", using the password and user listed in the **db/database.env** file.
- The **insert.py** file will create a new table in the "accounts" database called "users". The table should have an "ID" column, a "firstname" column and a "lastname" column. 
- The **insert.py** file will read the text from the **app/namelist.csv** file and in insert the information into the correct column. (Carefull, don't insert the header info!)

(NOTE- due to an issue with docker-compose, sometimes the python script runs before the database is started, causing an error. As an extra credit, add something to the scripts that makes the python script wait for the the database containter to be fully started!)

**Task Two** - Once the data from the CSV file is inserted into the database, add some code to the **insert.py** script that does the following:
- Read the data back out from the database, format the data as JSON, and save the JSON file to your local disk. This may require some changes to the other config files as well! 

Extra Extra Credit! Make your code handle exceptions! Can you run the script more than once? Can you update new data into the database? What else can you show? Have fun and good luck!
