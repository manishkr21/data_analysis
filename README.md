# data_analysis
This is to create documents and code for data analysis

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
openssl rand -base64 42
export SUPERSET_SECRET_KEY="generated files"
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
