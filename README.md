## Here are the steps to run the Python Flask app connected to a MySQL database that's uploaded on GitHub:

### 1. Clone the Repository:

First, clone the GitHub repository containing the Flask app to the local machineusing the git clone command:
```
git clone <repository_url>
```
	
### 2. Install Dependencies:
Navigate to the project directory and install the required dependencies. Use pip to install them from the requirements.txt file:
```cd <project_directory>
pip install -r requirements.txt
```
 
### 3. Set Up MySQL Database:
Ensure that MySQL server is running on the local machine. Create a new database for the Flask app (preferrably like "users_db").
**Go to mysql workbench**
```
create database users_db;
```
### 4. Configure Flask App:
Update the Flask app's configuration to connect to the MySQL database. Typically, this involves setting the database URI in the Flask app configuration.
 This could be done in a configuration file or directly in the Flask app script.
**app.py file**
 ```
 app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://root:12345678@localhost/users_db'
```
	
- Here 'root' is the mysql root , password -> 12345678, "users_db" is the database name created in the mysql.
	
### 5. Run the Flask App:
Run the Flask app using the following command:
```
python app.py
 ```
# 6. Access the App:
Once the app is running, open the web browser and navigate to the address where the Flask app is running
(usually http://localhost:5000 by default).

That's it! Your Flask app connected to the MySQL database should now be running locally on the machine.
