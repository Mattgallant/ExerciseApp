# Final Project (CS50Web 2020): Exercise Stats
This project was completed as the last project for Harvard CS50 Web class. I chose to create a web application, using **Django, Javascript and Python** that **display my running statistics in an interesting way**. In order to gain more practice with Javascript, I decided to make the webapp a **single page application**. I also learned more CSS by implementing animations on each page. I also got more hands on experience with reading documentation of a library I was not familiar with by using** Chart.js** for data visitualizaiton. The stats are pulled from my Garmin Connect watch which I use to record every run that I do. It is then automatically transferred to the Strava app where I then run a python script to pull from Strava's API and populate my sqlite database. Essentially, all I need to do to update the runs displayed on the site is just run a script. I also created an API so that I can use Javascript on the frontend to display my running data. With all of that set up, I have three main pages that display the data in different ways:
1. **Run List**: Displays all of my runs in a chronologicial fashion with relevant statistics. You can hover over any of the runs to see additional details. 
2. **Goals & Personal Records**: Displays my current running goals and my progress towards those goals. Shows current best times for various run distances. 
3. **Stats**: This page uses Chart.js to display my cumulative ran miles for the year and the miles I've ran per month. I may eventually add more stats like weekly miles ran and so on. 

## Files
**stava.py**: This is a script that pulls directly from the Strava API and updates the models in my database. Grabs the new run information, if any. 
**stats.js**: This is where the bulk of my code for the site is because it is a single page application. This file handles displaying a majority of my site. It works much like the email client project did. Inside are several functions that handle displaying the various pages based on button handlers that it sets up.
**theme.css**: This is where all of the styling for my site resides.
**layout.css**: A pretty light file. Just has some imports that I use in the head and sets up the basic HTML structure template.
**display.html**: This sets up the main display of my single-page app. It has some static HTML for each page and has divs for the stats.js page to load relevant content into. 

The rest of the files are mostly just Django default files that have not been edited very much. The only real function of interest is in **views.py** where I have set up an API function that returns a JSON object so that my frontend can access run data. 

**This web app is currently not hosted. Please visit this youtube link to see a video demonstration.** https://www.youtube.com/watch?v=qgztZabJmc0
