# week-3-Python-Sql-code-challenge

# Concerts Database Assignment

## Overview

This project involves managing a concert database with three primary entities: **Band**, **Venue**, and **Concert**. The objective is to interact with these entities through raw SQL queries, ensuring the code meets specific functional requirements. The assignment includes creating a database schema, defining relationships between tables, and implementing methods for managing and querying the data.

## Project Structure

The project is organized into the following files:

1.  **`db_database.py`**: Manages database connection and schema setup.
2.  **`band.py`**: Defines the `Band` class with methods to interact with band-related data.
3.  **`venue.py`**: Defines the `Venue` class with methods to interact with venue-related data.
4.  **`concert.py`**: Defines the `Concert` class with methods to interact with concert-related data.
5.  **`main.py`**: Provides examples of how to use the classes and methods to perform operations on the database.

## Setup

1.  **Install SQLite**: Ensure you have SQLite installed. SQLite comes pre-installed with Python, so no additional installation should be necessary.
    
2.  **Run Database Setup**: To create the database and tables, run the `setup_database()` function from `db_database.py`.
    
3.  **Populate the Database**: Use `main.py` to create sample data and test the functionality of the classes and methods.
    

## Code Explanation

### `db_database.py`

Handles database connection and schema setup. It includes:

-   **`get_db_connection()`**: Establishes a connection to the database and returns a cursor.
-   **`setup_database()`**: Creates the necessary tables for bands, venues, and concerts.

### `band.py`

Defines the `Band` class with the following methods:

-   **`__init__(self, id, name, hometown)`**: Initializes a `Band` instance.
-   **`concerts(self)`**: Returns all concerts associated with the band.
-   **`venues(self)`**: Returns all venues where the band has performed.
-   **`play_in_venue(self, venue, date)`**: Adds a new concert for the band at a specific venue on a given date.
-   **`all_introductions(self)`**: Returns a list of all introductions the band has made.
-   **`most_performances()`**: Returns the band with the most performances.

### `venue.py`

Defines the `Venue` class with the following methods:

-   **`__init__(self, id, title, city)`**: Initializes a `Venue` instance.
-   **`concerts(self)`**: Returns all concerts held at the venue.
-   **`bands(self)`**: Returns all bands that have performed at the venue.
-   **`concert_on(self, date)`**: Finds the first concert on a specific date.
-   **`most_frequent_band(self)`**: Returns the band that has performed the most at the venue.

### `concert.py`

Defines the `Concert` class with the following methods:

-   **`__init__(self, id, band_id, venue_id, date)`**: Initializes a `Concert` instance.
-   **`band(self)`**: Returns the band associated with the concert.
-   **`venue(self)`**: Returns the venue associated with the concert.
-   **`hometown_show(self)`**: Returns `True` if the concert is in the band's hometown.
-   **`introduction(self)`**: Returns the band's introduction for this concert.

### `main.py`

Provides examples of how to use the classes and methods:

-   **Create sample data**.
-   **Add a new concert**.
-   **Query concerts for a band**.
-   **Get introductions and hometown shows**.
-   **Find the band with the most performances**.

## Usage

1.  **Setup the Database**: Run the `setup_database()` function in `db_database.py` to initialize the database schema.
    
2.  **Create and Test Data**: Execute `main.py` to create sample bands, venues, and concerts. This script also demonstrates how to use the various methods to interact with the database.
    
3.  **Run**:
    
    css
    
    Copy code
    
    `python main.py` 
    

## Example Output

When running `main.py`, you might see output like:

csharp

Copy code

`Concert added for 'The Beatles' at 'Madison Square Garden' on 2023-09-20.
[(1, 1, 1, '2023-09-20')]
['Hello New York!!!!! We are The Beatles and we\'re from Liverpool']
True
The Beatles` 

## Notes

-   Ensure that SQLite is available and properly set up in your environment.
-   Adjust file paths and database names if needed to fit your local setup.

## License

This project is licensed under the MIT License. See the LICENSE file for details.