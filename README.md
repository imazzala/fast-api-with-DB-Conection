# fast-api-with-DB-Conection
Code created doing the FAZT's Fast API Course with MySQL DB Connection

This repository shows an example of a CRUD API with connection to a MySQL Data Base via SQL Alchemy. This basic CRUD can create, read, update and delete users in the Data Base. 

To run this project first you must clone this repo:

```
git clone git@github.com:imazzala/fast-api-with-DB-Conection.git
```

All the libraries are in the `requirements.txt` file. To install them, the following command must be executed:

```
pip install -r requiremets.txt
```

Before running the code, you must have a database created in MySQL. In this case, it is called `storedb`. In the [`db.py`](http://db.py/) file you must replace `root` and `pass`  and `storedb` with the user, the password and the name of your database in the engine variable:

```python
engine = create_engine("mysql+pymysql://root:pass@localhost:3306/storedb")
```

Once the engine variable has been configured, the server must be executed together with the app:

```python
uvicorn app:app --reload
```

And then the server must be open at the following IP Address: 

```python
127.0.0.1:8000
```
