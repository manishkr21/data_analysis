# data_analysis
This is to create documents and code for data analysis

Features of Apache superset
---------------------------
```
1. Data Visualization
2. Data Exploration
3. Data Analysis
4. Dashboards  ---- UI
5. Time Series Data
6. Authentication and Authorization
7. Integration with Databases
8. Extensibility and Scalability

```


Installing Apache Superset
--------------------------

1. Make sure you have install below packages
```
sudo apt-get install build-essential libssl-dev libffi-dev python-dev python-pip libsasl2-dev libldap2-dev default-libmysqlclient-dev
```

2.  Create a Virtual environment and activate it
```
Python3 -m venv venv
source venv/bin/activate
```

3. Install pillow & Apache Superset  package
```
pip install pillow
pip install apache-superset
pip3 apt-get install python3-setuptoools
pip3 install --upgrade pip
pip install --upgrade setuptools pip

```

4. Set Enviornment variables
```
export FLASK_APP=superset
```
5. Generate the secret key to set for flask based application
```
export SUPERSET_SECRET_KEY=$(openssl rand -base64 42)
```

6. Initialize the database
```
superset db upgrade
```

7. create user, required to sign in into the application
```
superset fab create-admin
```

8. (Optional) Load some Examples to play with apache-superset
```
superset load_examples
```

9. Create default roles and permissions
```
superset init
```

10. To start the development server on port, use -p to bind to another port
```
superset run -p 8099 --with-threads --reload --debugger
```

11. Open URL to access the application
```
HTTP://localhost:8099
```

12. To start if already setup
```
export FLASK_APP=superset
superset run -p 8099 --with-threads --reload --debugger
```

## To connect with MySQL Database
1. Make sure we have essentials packages
```
sudo apt-get install python3-dev default-libmysqlclient-dev build-essential pkg-config
```

2. Install MySQL
```
sudo apt-get install pkg-config


pip install mysqlclient 
pip install cx_Oracle 
pip install snowflake-sqlalchemy 
pip install pymssql 
pip install pyhive 
pip install sqlalchemy-redshift
```
3. Now you can Access your MySQL Database
