# kino-wecg
A Python web-scraper to retrieve IMDB information for movies

# Purpose
This scraper was built for a class project that required getting IMDB information for the 500 most popular movies (as determined by number of ratings) for each year 2010 - 2020.
The ultimate goal of the project was to gain insights into attributes that might factor into a critically successful movie, as well as attempting to build a prediction model for critical ratings.

# Building & Use
PythonPackages used include: BeautifulSoup, pandas, requests, numpy, time, re, and random.

The scraper iterates through pages of 50 entries each to retrieve the wanted information. The amount of entries can be changed easily to include more or less.

To change which year is being scrapped, the user must manually change the dates in the URL:
![image](https://user-images.githubusercontent.com/68206893/109361771-3b71df00-784f-11eb-8bee-327edbb6d093.png)


![image](https://user-images.githubusercontent.com/68206893/109361472-96570680-784e-11eb-96c3-13d7e91f1b79.png)

![image](https://user-images.githubusercontent.com/68206893/109361495-a1aa3200-784e-11eb-9733-4f7c55091323.png)

A loop then iterates through multiple web pages, retrieves text values and appends the appropriate lists.

An example:
![image](https://user-images.githubusercontent.com/68206893/109361635-f483e980-784e-11eb-85a4-f108a075b350.png)

Once the information for the movies has been put into the appropriate lists, a dictionary is created to map the lists to columns within a data-frame.
![image](https://user-images.githubusercontent.com/68206893/109361844-6a885080-784f-11eb-8eb9-2a046dbf4f10.png)

This data-frame can then be written to a .csv or other file.
