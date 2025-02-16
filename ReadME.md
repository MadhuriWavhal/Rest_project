## Step 3: Set Up the Project on Office PC

### Navigate to the project folder:
```sh
cd myrestproject
```

### Create a virtual environment:
```sh
python -m venv env
```

### Activate the virtual environment:
#### Windows:
```sh
env\Scripts\activate
```
#### Mac/Linux:
```sh
source env/bin/activate
```

### Install dependencies from requirements.txt:
```sh
pip install -r requirements.txt
```

### Apply migrations (if using a database):
```sh
python manage.py migrate
```

### Run the development server:
```sh
python manage.py runserver
```

---

## 🚀 Step 4: Database Considerations

### If using SQLite, just copy the `db.sqlite3` file.

### If using PostgreSQL/MySQL, backup and restore the database:
#### On personal PC (Backup Data):
```sh
python manage.py dumpdata > data.json
```
#### On office PC (Restore Data):
```sh
python manage.py loaddata data.json
