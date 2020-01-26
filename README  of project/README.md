<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# Around the corner
*Valerie Stroh, Senan Jadeed, Tobias Glinzer*

*Data Analysis January 2019, Berlin, 2020-01-25*

## Content
- [Project Description](#project-description)
- [Questions & Hypotheses](#questions-hypotheses)
- [Dataset](#dataset)
- [Database](#database)
- [Workflow](#workflow)
- [Organization](#organization)
- [Links](#links)

## Project Description
In this project we wanted to focus on a topic related to tourism. We chose to compare Airbnb listings with hotels in Berlin, Germany. As Airbnb and hence the number of available apartments through its service has grown tremendously over the last years, it has become an alternative for tourists/business travelers that need a place to stay overnight. Therefore, we compared hotels and Airbnb listings with each other to find differences/similarities between those two.

## Questions & Hypotheses
As written before, the number of Airbnb listings has grown over the last years. Today it seems that just based on the number of available rooms in Berlin, booking a room on Airbnb is a true alternative to booking a hotel room.
The questions/assumptions we have are:

1. How is the number of Airbnb listings compared to the number of hotels throughout the city in the different areas?
        We assume that Airbnbs are more likely to be found in residential areas, where as hotels also cover business                   districts/more central districts.

2. How do the prices per area compare to each other? Do higher hotel prices in some areas also mean higher prices per night in an Airbnb apartment? 
        Expensive hotels are most likely in areas with high rents, resulting in an increased average price per night for an           Airbnb apartment in this area.

3. Over all, you might assume that the average price per night in an Airbnb apartment is less than the average price per night in a hotel as you get less service. But is that true? 
        Our assumption is that the average price per night in an Airbnb apartment is less than the 
        price per night in a hotel.
        



## Dataset
To analyze those questions, we will work with data from different sources that provide us with
1. Price per night (for 2 persons)
2. Area/district in Berlin
for both - Airbnb listings and hotels.

We used the following three sources:

Airbnb listings - API - data include: Airbnb listings worldwide (we reduced it to Berlin), data include price per night, area, name of owner, geolocation, cleaning fee, no of persons, description of apartment and more.
[Link to API used](https://public.opendatasoft.com/explore/dataset/airbnb-listings/api/?disjunctive.host_verifications&disjunctive.amenities&disjunctive.features&rows=1000&refine.city=Berlin&dataChart=eyJxdWVyaWVzIjpbeyJjaGFydHMiOlt7InR5cGUiOiJjb2x1bW4iLCJmdW5jIjoiQ09VTlQiLCJ5QXhpcyI6Imhvc3RfbGlzdGluZ3NfY291bnQiLCJzY2llbnRpZmljRGlzcGxheSI6dHJ1ZSwiY29sb3IiOiJyYW5nZS1jdXN0b20ifV0sInhBeGlzIjoiY2l0eSIsIm1heHBvaW50cyI6IiIsInRpbWVzY2FsZSI6IiIsInNvcnQiOiIiLCJzZXJpZXNCcmVha2Rvd24iOiJyb29tX3R5cGUiLCJjb25maWciOnsiZGF0YXNldCI6ImFpcmJuYi1saXN0aW5ncyIsIm9wdGlvbnMiOnsiZGlzanVuY3RpdmUuaG9zdF92ZXJpZmljYXRpb25zIjp0cnVlLCJkaXNqdW5jdGl2ZS5hbWVuaXRpZXMiOnRydWUsImRpc2p1bmN0aXZlLmZlYXR1cmVzIjp0cnVlLCJyb3dzIjoiMTAwMCIsInJlZmluZS5jaXR5IjoiQmVybGluIn19fV0sInRpbWVzY2FsZSI6IiIsImRpc3BsYXlMZWdlbmQiOnRydWUsImFsaWduTW9udGgiOnRydWV9&location=13,52.48848,13.15063&basemap=jawg.streets)

Expedia listings - Web Scraping - data include: hotels in Berlin, price per night for 2 persons, area
Method used: Selenium, scraping the following site:
[Link used to scrape Expedia](https://www.expedia.de/Hotel-Search?adults=2&destination=Berlin&endDate=2020-02-06&rooms=1&&startDate=2020-02-05)


Booking.com data - gathered through Octoparse - data include: hotels in Berlin, price per night for 2 persons, area

Link: Worked inside Octoparse app but narrowed results according to our specifications


## Database
We created three tables from the three different sources.
Those tables have been merged after cleaning, as they were reduced to four columns so that the formats match:
1. name (of hotel/ID of airbnb listing)
2. price per night
3. area 
4. source (airbnb/ booking.com/ expedia.de)

(+ in case of merging the two tables with hotel data, duplicates within those data have been removed previously)

## Workflow
The workflow was as follows:
1. Definition of topic and gathering possible data sources
2. Definition of questions that can be asked/topics that can be analyzed
3. Comparing data sources and decision which data sources to use
4. Extracting the data through API/Web scraping (if possible, strong data in GitHub repository)
5. Cleaning data
6. Merging data
7. Running analysis with those data to gain insights (to our questions), incl. use of plots
8. Preparing presentation based on our insights (Google slides)
9. Finalizing folder and file structure


## Organization
For communication we mainly used:
1. Slack

After definition of topic we set up
1. GitHub repository
2. Kanban board (using Trello)

For gathering possible data sources everyone worked on his own.
Extracting data required a lot of collaboration so that most of the time at least two person worked on the same topic/data source.
After we had the data we split up the work, defined tasks, used Trello intensively.

The repository is set up as follows:
Folder structure: 

### Output folder:
[Merging, Analysis and Plotting]

[Readme]

### Subfolder with following content:
##### 1. Data Sourcing: 

[AirBnB](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/2020-01-24_API_Request_Airbnb.ipynb)

[Expedia](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/Expedia_webscraping.ipynb)

[Booking.com](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/BookingcomHotelsinBerlin.csv) - we used [Octoparse](https://www.octoparse.com/), so no coding was needed

##### 2. Data Cleaning:

[AirBnB](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/2020-01-24_API_Request_Airbnb.ipynb) (same file as for data sourcing)

[Expedia](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/Expedia_cleaning.ipynb)
Uses this

[Booking.com](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/Booking_data_cleaning.ipynb)


##### 3. Export files (*.csv* or *.pkl*):

Export from Octoparse:
[Octoparse csv - see above, this is the same file as mentioned for data sourcing from Booking.com data](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/BookingcomHotelsinBerlin.csv)

Export from AirBnB data extracting and cleaning:
[AirBnB csv](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/2017_airbnb_api_data_clean.csv)

[AirBnB pkl - used for final analysis](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/2017_airbnb_api_data_clean.pkl)

Export from Expedia data scraping:
[Expedia results csv](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/results.csv)


Export from Expedia data cleaning:
[Expedia data csv - used for final analysis](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/data_clean.csv)


Export from Booking.com data cleaning:
[Booking.com csv](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/Booking_price_comparison.csv)

[Booking.com pkl - used for final analysis](https://github.com/valsophie/group_project-/blob/master/Notebooks%20for%20scraping%2Bcleaning%20and%20raw%20data/Booking_price_comparison.pkl)


#### Further files in folder:

**chromedriver** and **chromedriver.exe** - those files are needed to run the Expedia web scraper on Windows/Mac/Linux 


## Links

[Repository](https://github.com/valsophie/group_project-)  
[Slides](https://docs.google.com/presentation/d/1QMRnM0o_aV_7aZIWNFUo00PV0I9q8726zbdpKV6Djf0/edit?usp=sharing)
[Trello](https://trello.com/b/NqMasWcp/data-thieves-kanban-data-01-20-project3-group2)  
