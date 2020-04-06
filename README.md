# World Weather Analysis

In this repo, we used our API keys to get weather and Google maps information. With the weather information, we plotted the data in scatter plots and displayed linear regression for more information.

## Resources

   - Data Source: Open Weather Map, Google Maps 
   - Software: Python 3.7.6, Jupyter Lab 1.2.6
   - Library: Matplotlib.pyplot, Pandas, NumPy, Requests, SciPy.stats, Datetime, Time, Citipy, Gmaps
   
## Challenge

Working with the PlanMyTrip app, you are asked to do the following:

   1. A weather description to the pop-up markers for customers so that they know what the weather is as they are traveling.
   2. A notation in the search criteria to indicate if it is raining or snowing for customers who are making travel decisions in real-time.
   3. A map that shows the directions for customers’ travel itinerary.
   
### Part 1

Within this part, we are getting the Weather Description and Amount fpf Precipitation for each city.

- We generated 1,500 random latitudes and longitudes and found the nearest city to each combination
- We iterated through the list of cities and collected the following information.
    - Latitide and Longitude
    - Maximum temperature
    - Percent humidity
    - Percent cloudiness
    - Wind speed
    - Weather description
- We used a try-except block and collected the amount of rainfall and snowfall in inches for the last three hours.
- After we collected all the information, we added the data to a new DataFrame and saved it as a CSV file.

### Part 2

In Part 2, we uploaded the CSV file we saved in Part 1 and filtered through the DataFrame with *input()* for the following.

1. The minimum temperature preference
2. The maximum temperature preference
3. Does the customer want rain (yes/no)
4. Does the customer want snow (yes/no)

- In order to get this information, we used *if*, *elif*, and *else* statements to account for all the possible answers.
- One thing to note, if the answers do not pull any information, there will not be an error statement. Instead, it will output an empty DataFrame.
- To account for this, we put an *if* statement to catch the empty DataFrame and print a message indicating, 'No cities matched your criteria.'
- We saved the DataFrame to a new CSV file.
- Created a marker layer map showing all the cities in the new DataFrame on the map.
- Created a text box displaying the hotel and weather information for each marker.
- Saved both images as a .PNG file.

### Part 3

In the last part, we picked at least 4 cities that were close to each other and ensured that the Directions API has been enabled on the Google Maps Platform.

- We created separate DataFrames for each city we chose and created a variable for the latitude and longitude coordinates.
- Created a directions layer map with the coordinates, specifying the *travel_mode* as 'DRIVING'.
- We then saved the directions layer map as a .PNG file.
- We then combined all the separate DataFrames into a new DataFrame.
- We created a marker layer map to display pop-up marker that contains the following information.

    - Hotel name
    - City
    - Country
    - Current weather description with the maximum temperature
    
- Once displayed, we took a screenshot and saved the pop-up marker map as a .PNG file.

## Usage

If you would like to use this file: 

- Ensure you have the required software to run these files.
- Download the *.ipynb* and *.csv* files.
- You will need your own API keys. (You can sign up for a free one on each site. Google will ask for a credit card for your account but will not charge your account until your choose to change your plan)
- When you have your API keys, save them in a separate file to ensure that no body can access your keys.
- To load the key into your file, use the following code.

  > from (.ipynb file) import (API key name)
  
- Pay close attention to how many times you use your key, as the number of times you make a request is limited to which prescription you have chosen for your account.

