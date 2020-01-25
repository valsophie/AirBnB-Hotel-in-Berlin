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
In this project we wanted to focus on a topic related to tourism. We chose to compare Airbnb listings with hotels in Berlin, Germany. As Airbnb and hence the number of available apartments through its service has grown tremendously over the last years, it has become an alternative for tourists/business travelers that need a place to stay overnight. Therefore, we compared hotels and airbnb listings with each other to find differences/similarities between those two.

## Questions & Hypotheses
As written before, the number of Airbnb listings has grown over the last years. Today it seems that just based on the number of available rooms in Berlin, booking a room on Airbnb is a true alternative to booking a hotel room.
The questions/assumptions we have are:

1. How is the density of Airbnb listings compared to the density of hotels throughout the city? Does a higher number of hotels in a specific area correlate to a higher number of Airbnb apartments? 
        We assume that there might be a negative correlation as hotels might not be in residential areas.

2. How do the prices compare to each other? Do higher hotel prices in some areas result in higher prices per night in an Airbnb apartment? 
        There might be a positive correlation as expensive hotels are most likely in areas with high 
        rents, resulting in an increased average price per night for an Airbnb apartment in those areas.

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

Link: **INSERT MISSING LINK**


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
Folder structure: **Describe folder structure**
File structure: **Describe file structure**


## Links


[Repository](https://github.com/valsophie/group_project-)  
[Slides](https://slides.com/)  **Insert link to slides**
[Trello](https://trello.com/b/NqMasWcp/data-thieves-kanban-data-01-20-project3-group2)  
