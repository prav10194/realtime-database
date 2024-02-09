# Realtime Database
Setting up Realtime Database for Python. Will be setting up a simple database for documentation. 


#### Creating it om GCP

#### Setting up the database in Python

```python
import firebase_admin
from firebase_admin import credentials, db

# Enter the path for secret key json
cred = credentials.Certificate('<filepath>.json') 

firebase_admin.initialize_app(cred, {
    'databaseURL': "https:test.firebaseio.com/"
})

ref = db.reference('<db name>')
````

#### Read + Filter

```python
snapshot = ref.order_by_child('key').equal_to('value).get()

for key in snapshot:
  text += str(key)
```
