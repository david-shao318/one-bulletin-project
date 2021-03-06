# one bulletin

https://one-bulletin.herokuapp.com/

A mini-project using django.

Aggregates news headlines from several news media RSS feeds.

This is a work-in-progress. The app is currently configured to only access specific CBC, New York Times, and Economist feeds. This is done every fifteen minutes to update the database. A selection form for the webpage to filter news stories and multiple time zone support are yet to be implemented.

The app is currently hosted on Heroku and uses the default PostgreSQL database on the server. Please note that requesting the page for the first time may take a while since Heroku shuts down the server after thirty minutes of inactivity.

## How to Run Locally

Use Python 3.9 or later (this project was developed using Python 3.10.2).

Create and activate a virtual environment. Then run `pip install -r requirements.txt` to install all required packages.

In `project_one_bulletin/settings.py`, set `DEBUG = True`. Uncomment the `SECRET_KEY` used for testing.

Now, run `python manage.py makemigrations && python manage.py migrate` to initialize a local database.

Install the `git` and `heroku` CLIs.

Run `heroku local --port=8000` to test. Go to `0.0.0.0:8000` (or `0.0.0.0:8100`) in a browser.
