# Car Registry App

This is a Python code snippet for a car registry application developed using Streamlit and SQLite. The application allows you to add, view, update, and delete car and driver records in a SQLite database.

## Prerequisites
- Python 3.x
- Streamlit
- SQLite

## Installation
1. Make sure you have Python installed on your system.
2. Install the required packages by running the following command:

pip install streamlit sqlite3


## Usage
1. Save the code in a file (e.g., `car_registry.py`).
2. Create a SQLite database file named `cars.db` in the same directory as the code.
3. Open a terminal or command prompt and navigate to the directory containing the code and the `cars.db` file.
4. Run the following command to start the Streamlit app:
streamlit run car_registry.py

5. The application will open in your web browser.

## Features
The car registry application provides the following features:

### 1. Add a new car and driver
- Select a car model from a list of available models.
- Set the year of production (not earlier than 2015) using a slider.
- Choose a car registration from a list of available registrations.
- Select a name and surname for the driver from pre-defined lists.
- Enter the driver's phone number and birthday.
- Click the "Add" button to add the car and driver to the database.

### 2. View all drivers and their cars
- Displays a list of all drivers and their associated cars.
- Allows you to select a driver from the list to view their details.

### 3. Delete a driver and their car
- Enter the ID of the driver you want to delete.
- Click the "Delete" button to remove the driver and their car from the database.

### 4. Update a car and driver
- Enter the ID of the car you want to update.
- If the car ID exists, it displays the current details of the car.
- Allows you to modify the car model, year, and driver details.
- Click the "Update" button to update the car and driver information in the database.

## Database Structure
The application uses a SQLite database named `cars.db` and consists of two tables: `cars` and `drivers`.

### Table: cars
- Columns:
- id (INTEGER PRIMARY KEY AUTOINCREMENT)
- model (TEXT)
- year (INTEGER)
- registration (TEXT)
- driver_id (INTEGER, FOREIGN KEY REFERENCES drivers(id))

### Table: drivers
- Columns:
- id (INTEGER PRIMARY KEY AUTOINCREMENT)
- name (TEXT)
- surname (TEXT)
- phone (INTEGER)
- birthday (TEXT)

## Notes
- The application assumes that the `cars.db` file exists in the same directory as the code file. If the file doesn't exist, the application will create a new database file with the provided name.
- The code uses the Streamlit library to create a user-friendly interface for interacting with the car registry application.
- The SQLite database operations are performed using the `sqlite3` module in Python.
- The code includes helper functions to add cars and drivers, delete drivers, and update car and driver information.
- The application uses lists of predefined car models, years, names, surnames, and registrations for user input options.
- The main function `main()` is called when the script is executed, and it contains the Streamlit app logic.

Feel free to explore and modify the code according to your needs. Enjoy using the Car Registry App!
