# Project title
Scraping the information you need in your daily life with Python

# Motivation
To solve the incovenience of daily life by scraping information at once that we have to check on different sites every day

# Installing
1. pip install requests  
Connected to the site by using requests module in order to get response from server.   

## Following are the sites.  
  -
  -
  -
  -

2. re  
To find the string (tag element) starting with certain character.

3. pip install beautifulSoup4
To get the needed tag element from HTML code.

# Code
Created 4 functions. Following is the explanation of the core code for each function.
1. def scrape_weather()  
~~~
    curr_temp=soup.find("p", attrs={"class":"info_temperature"}).get_text().replace("도씨", "")
~~~
To get the current temperature, find "info_temperature" class in < P > tag and get text. Use replace( ) function to delete the word "도씨".  
~~~
    morning_rain_rate=soup.find("span", attrs={"class":"point_time morning"}).get_text().strip()
~~~
To get the morning rain rate, find "point_time morning" class in < span > tag and get text. Use strip( ) function to remove blank.
~~~
   dust=soup.find("dl", attrs={"class":"indicator"})
~~~
~~~
   pm10=dust.find_all("dd")[0].get_text() 
~~~
To get the brown smog rate, find "indicator" class in < dl > tag. Find all the < dd > tag in < dl > tag and select the first index. 

# Running the tests
![img1](https://user-images.githubusercontent.com/77823753/108456197-262b0c80-72b3-11eb-967a-feac102ff0ec.PNG)
