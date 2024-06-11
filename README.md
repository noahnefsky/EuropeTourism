# Data Visualizations of Europe Tourism

### Dataset

Europe Commercial Air Flights and Passengers, [Link](https://www.kaggle.com/datasets/br33sa/europe-commercial-air-flights-and-passengers/data?select=Passengers_Month.csv)

The dataset we will explore is about Europe Commercial Air Flights and Passengers from 1993-2022. Specifically, we will be looking at the passengers per month that flew to each country. Each data point contains metadata for the country, if it was national, international or total, the month, the year and number of passengers in the month. We have acquired the data from Kaggle though it was initially created by Eurostat, the statistical office of the European Union.

Given the dataset was initially put together by Eurostat, it is a reliable source. The specific dataset on Kaggle modified the original one to only show the number of passengers per month, whereas the one from Eurostat has uncleaned data about the passengers and flights per year, month and quarter. The process the Kaggle author took to clean the dataset and form the one we are using is posted on Kaggle. It is very standard and matches the initial Eurostat data, so the dataset is dependable.

The dataset has some points where the passengers total is missing, though there are still over twenty-thousand usable points. The years that have the most usable points are 2005-2021, so we will remove the 1993-2004 and 2022 years from the dataset. Additionally, we will also filter for the points in which flights come from international origin, as we want to focus on tourist based travel and overall non-local population in a country per month. After filtering the data to the years 2005-2021 and international origin, our dataset will still consist of over 6000 points. This will allow us to make meaningful visualizations based on reliable data.

### Why is this useful?

The tourism industry in Europe generates a lot of income for many different countries. Europe receives hundreds of millions of tourists each year which oftentimes leads to crowding, especially near tourist attractions. Some people do not mind the clutter, yet many tourists struggle to find the right time to visit a country in Europe when it is least touristy. Some people feel the experiences are diluted when countries are overrun with tourists and that it takes away the authentic feeling of visiting a new country.

We aim to find when each country’s tourism is in its peak season and has a high population of tourists and when it is in its low seasons where less tourists are present. Our visualizations will express this by showing the concentrations of passengers who fly international to each European country throughout each month of the year. We address the following three questions:
1. How busy is each country each month or the year with visitors from other countries?
2. When are the peak and low seasons for tourism in each European country?
3. How does the number of passengers entering each country change throughout the year?

Our target audience is travelers seeking more information about countries they wish to travel to. Hopefully, these visualizations and our discoveries will help them choose the best destinations and times based on their interests. Either they trust the crowd and want to follow the touristy trends or they wish to go at a time when a country is in its most authentic state. Overall, by visualizing the flow of passengers into a country each month, we will be able to better deduce peak season in contrast to low season and uncover useful information for tourists to help them make decisions based on their preferences.


### Exploratory Data Analysis

The raw data of the monthly air passengers per country contains: 35 unique countries, 3 different coverages (national, international, total), years (1993-2022), months (M01-M12), and total number of passengers on board. The dataset has some points where the passengers total is missing, though there are still over twenty-thousand usable points after we remove the NaN values. The years that have the most usable points are 2005-2021, so we will remove the 1993-2004 and 2022 years from the dataset. Additionally, we will filter for the points in which flights come from international origin, as we want to focus on tourist based travel and overall non-local population in a country per month. After filtering the data to the years 2005-2021 and international origin, our dataset will still consist of over 6000 points. This will allow us to make meaningful visualizations based on reliable data.

The following displays the unprocessed data, the processed data, and finally the average of the passengers per month of each country for all the years of data available. It orders the passengers per month so you can see which country and month combinations are the most popular and the least popular.

<img width="325" alt="unprocessed" src="https://github.com/iniyam/com-480-EuropeTourism/assets/62399852/b6cd6a02-df45-4a5d-b8d2-5460929fe1f4"><img width="325" alt="procesessed" src="https://github.com/iniyam/com-480-EuropeTourism/assets/62399852/fca9f763-b4b3-46bd-a92c-0f2941a6a4b9"><img width="175" alt="avg" src="https://github.com/iniyam/com-480-EuropeTourism/assets/62399852/42282c46-d975-4db9-b424-b65878d02d3a">


The following plots the averages across the years of the number of passengers in each country per month into a visualization. You can see from the graph that July & August (months 7 & 8) tend to have the most passengers flying in compared to other months regardless of country. And, you can see by country GBR, DEU, ESP have the highest amounts of passengers respectively and FRA, ITA, TUR are the next closest as well.

<img width="400" alt="1" src="https://github.com/iniyam/com-480-EuropeTourism/assets/62399852/810b06e1-c207-4ef8-ae2c-88cd108f6082">


<img width="400" alt="graph" src="https://github.com/iniyam/com-480-EuropeTourism/assets/62399852/7464b26c-e68c-4153-8259-be07d831b3fc">


### Visualization 1 Overview:

This visualization allows the user to see how busy a country is with tourists in each given month and how it changes throughout the years. Users can explore the data through an interactive map and slider. 

**Key features include:**
1. _Map Representation_: A map of Europe displaying countries colored according to tourist "busyness," with darker red indicating /”hotter” tourist activity and lighter red indicating lower/”less hot” activity.
2. _Interactive Slider_: Users can select a specific month to observe changes in tourist activity throughout the year.
3. _Year Selection_: Users can choose between viewing the average tourist activity from 2005 to 2020 or select a specific year within that range.
4. _Hover Information_: Hovering over a country reveals the total number of international passengers arriving in that country for the selected month.

This visualization aids users in easily identifying the busiest tourist destinations in Europe for any given month, easily seen by the “hot” and “less hot” regions.

### Visualization 2 Overview:

This visualization allows the user to select a country and look at the distribution of international passengers flying into that country over all 12 months of the year through a star graph. The design of the star graph allows for users to compare popular vs uncrowded months, as well as visualize the changes over each of the 4 seasons in a year.

**Key features include:**
1. _Interactive map_: Users are able to select the country they desire. As soon as a country is selected, it is highlighted in green to display the geographic region relevant to the respective star plot.
2. _Star Plot_: The appropriate data (i.e. average number of flights across the years 2005-2021 of the number of passengers in each country per month) is shown as a star graph with 12 partitions, one for each month of the year.
3. _Hover Information_: Hovering over a particular data point in the star graph reveals the total number of international passengers arriving in that month for the currently selected country.
4. 

## Finished Product

<a href="https://com-480-data-visualization.github.io/EuropeTourism/#viz1">Website</a>


### Setting up the project
- Step 1: Check if the project can be opened. If not, go to step 2; otherwise go to step 3.
  - Note: It is recommended to open the project via IntelliJ or any other JetBrians product (since they set up a webserver when opening the index.html file).
- Step 2: Setting up a webserver
  - Note:  In order to load the .json files, one might face "CORS-Policy" problems. In order to prevent this, a local webserver is needed. This can be achieved by these 3 steps:
  - A: Installing the needed NPM module (we assume that NPM is already installed): ```npm install -g http-server```
  - B: Creating a webserver by running ```http-server -p 8000```
  - C: Open ```http://localhost:8000/``` in the browser; all files should be loaded and the first map(i.e. visualization 1) should be visible

### Technical Setup
Technologies used:
  - HTML, CSS
    - CSS: Bootstrap 5 was used by importing a CDN. We used this approach to have a basic skeleton for our grid system and the navigation bar.
  - JavaScript
    - TopoJSON & D3.js: as previously described in Milestone 2, this was needed for the implementation of Visualization 1 and Visualization 2 as well.
    - jQuery: for various DOM Operations (e.g. selecting/adding DOM-nodes)
    - Map.js: includes logic for Visualization 1
    - StarPlot.js: includes logic for Visualization 2

### 3. Intended Usage of both Visualizations
#### Visualization 1
  - Click on "Passenger Map" (Visualization 1) in navigation bar 
  - Users should try out the following options/interactions
    - Change the year via the dropdown menu
    - Change the month via the slider
    - Change from proportional data to total data by clicking on the respective buttons
    - Hover over countries to receive detailed information about the passenger numbers

#### Visualization 2
  - Click around in "Monthly Passenger Star Plot" (Visualization 2) in navigation bar
  - Users should try out the following options/interactions
    - Hover over a point of Europe to see the related country highlighted in light green
    - Select a country by clicking on it. The country is marked in dark-green and the full name of the country is displayed in the text above the map.
    - The star plot right next to the map shows the aggregated monthly passengers in light green

- Visualization 2
  - Germany, UK, France, Spain (Example for large population): Generally high amount of passengers, especially in summer
  - Greece, Turkey (Example for tourist regions): Drastic increase during summer months, very similar to one another.
  - Sweden, Austria (Smaller countries): Seem to have rather stable amount of passengers across the whole year, still increase in summer though
  - Norway/Sweden: Despite northern lights: No increase in flight passengers in winter (when northern lights are visible the most)
