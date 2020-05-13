# NYC Vehicle crashes 


Since 2012 more than 1,000,000 traffic accidents have occured in New York. As a result of those accidents around 200,000 people have gotten injured. In fact, traffic incidents are the leading cause of injuries in New York City. The aim of this project is to visualize, analyze and model the traffic incidents in order to find identifiable patterns that could aid the process of reducing the risk of injuries in New York City. To enable this, the Motor Vehicle Collisions data sets from NYC database is used (the data can be found here: [Crash Data](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95), [Vehicle Data](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Vehicles/bm4k-52h4) and [Persons Data](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Person/f55k-p6yu)).

More specifically, we ask the following questions; 

* Where and when are the crashes happening? 
    * Based on the different boroughs in NYC, the GPS locations and time and day of the crashes.
* What are the leading causes of these accidents?
    * Alcohol involvement and outside-of-the-car distractions are looked into.
* What vehicles are often involved?
    * A large number of vehicle types are reported in the crash data sets.


All vizualisations generated in this study can be found at INSERT REF EXP NOTEBOOK.


## New York through data
As mentioned, lots of car crashes happen every day in NYC. In fact, so many happen that we are able to visualize the entire city just based on the GPS location of the individual crashes, when we sample over the 8 year span in which the data has been gathered (2012 - 2020). From the map below, we can recognize some of NYCs famous features such as Central Park in Manhattan (the black square in the left-most area) and the Hudson river which encircles the Manhattan peninsula. 

<iframe src="map.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="520"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>


By using the data freely available to us, we hope to broaden ours and yours understanding of the city based solely on the car crash data sets. A big task, we know, but stay with us!

## Basic statistics 
The goal of the following visualizations are primarily to get you, the reader, up to speed on how the distribution of car crashes looks like in NYC. What is the maximum number of people killed in a single car crash? What is the maximum number injured? How does the different age groups fare in the statistics? Where does the most of the car crashes happen? Lots of plots, but they hide some very interesting information if analyzed a bit!

### Injuries and distribution in the boroughs
Using the data sets, we have plotted the number of persons, pedestrians, cyclists and motorists injured along with the number of persons killed on a logarithmic plot. This gives us a feeling for how many crashes are severe in a sense that they inflict injuries or even deaths. Fortunately, most crashes across all the trafic groups are seen to be non-lethal and even non-harmful. But still, a significant number of them result in an injury, and a few of them even have multiple people injured. If we look at the last columns of the persons, pedestrians and motorist plots, we can see a few which have a lot of people involved in the crash (43 persons injured in the same car crash!).

![Injuries](injuries_seaborn.png)

Furthermore, the number of trafic accidents across the 5 boroughs in NYC are plotted in a bar plot, showing that Brooklyn has the highest number of car crashes when we count them up over the 8 year time span.

<iframe src="yearly_borough.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="325"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Building upon the crashes in the boroughs, we have plotted the yearly development for each borough, where the succes in reducing the number of crashes for i.e. Manhattan can be seen. This could be due to a program initialized in 2014 called 'Vision Zero', which was aimed at reducing the amount of injuries related to vehicle accidents. A link to the program can be found [here](https://www1.nyc.gov/content/visionzero/pages/). This program continues to this day, and employs increased trafic control (harder penalties for speeding, failing to yield to pedestrians etc.). As such, it wouldn't surpise us if this is the cause of this drop in injuries.

### Crash distribution heatmap
Now we move on to the more number-heavy plots, where the number of crashes in each month (1 being January and 12 being December) are shown for the time period 2012-2020.

![Heat map](output.png)

The thing worth noticing here is the smaler amount of accidents early in the year and the increase in reported 
accidents from 2015 to 2018 (the increase in dark colors). The summer of 2016-2018 saw an increase of around
1500-2000 accidents compared to earlier years. It is dificult to predict what the main contributing factors were here. 
Our initial guess was that higher temperatures in this period could contribute to higher outside traffic. However,
according to the National Wheather Service, the summers of 2016-2018 in New York where not distinctly warmer than previous
years [Central Park annual temperatures](https://www.weather.gov/media/okx/Climate/CentralPark/monthlyannualtemp.pdf). In reference to the 'Vision Zero' program, another explanation could be that the program was not very succesful, or that the program has increased general trafic awareness leading to an increase in reported/registered accidents corresponding to the effectiveness of the employment of the program.


### Magnus' tekst del
In 2014 New York initialized a 'Vision zero' program aimed at reducing the amount of injuries related to 
vehicle accidents [Vision zero](https://www1.nyc.gov/content/visionzero/pages/). 
This could either mean that the program was not very succesfull or that this program increased awareness around vehicle accidents leading to more accidents beeing registered/reported without a significant change in actual accident numbers.


## Age group and gender distribution
Now, we look into another part of the data set, namely the data about the people involved in the crash. We have chosen to look at the drivers of the vehicles involved in the crashes, more specifically their age and genders, to attempt to discern if there are any patterns. The drivers are split into age groups for each gender (male/female), which are then normalized by the actual number of people in NYC within that age group (specific numbers are found [here](https://www.baruch.cuny.edu/nycdata/population-geography/age_distribution.htm)). This gives us a realistic method of comparing the number of crashes per people now found in each bar to a bar in a different age group. However, as we dont know how many people in a given age group have a drivers license and own a vehicle, there's still some error here, but we have unfortunately not been able to find such numbers.

<iframe src="Crashes_agegroups.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="525"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

We all know the prejudice about young males and fast cars, but there's actually something to it! We can see a vast majority of the crashes has a male driver between the age of 20 and 24 involved in the crash, whereas the older males has a significant lower amount of car crashes to their names. Funnily enough, we can see the same trend for young females! We can see that young males in this age group are involved in more than 3 times the amount of car crashes compared to their female counterparts, but when we look at the trend for females themselves, they also appear to be involved in more crashes when compared to their older age groups. As such, the same trend is visible for both males and females.

## Spatial distribution of the car crashes
Phew, that was a lot of static bar plots! I think it's time for some interactive plots. In the following map, we have plotted the individual crashes on a Google Maps looking plot, where each crash is categorized by where it happened, how many people got injured in the crash, why the crash happened and what kind of vehicle was involved. The color of the initial circles represent the density of crashes, wh
<iframe src="interaktivfoliummap.html"
    sandbox="allow-same-origin allow-scripts"
    align = "right"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

<iframe src="interaktivfoliummap.html"
    sandbox="allow-same-origin allow-scripts"
    align = "right"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>


Have a look around, and try to see if you can spot some of the interesting cases we talked about earlier (Hint: the 43 persons injured crash happened on Herkimer Street in Brooklyn, which can be found west of the Cemetery of the Evergreens along Atlantic Avenue).

### Dangerous roads
We now turn our attention to the roads in New York. It is expected that some roads are more prone to have accidents than others,
due to factors like heavy traffic, poor road conditions, traffic nodes etc. 
The figure below shows the roads with the highest accident counts for each borough.

<iframe src="Dangerous.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="450"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

For near all boroughs, there are one or two roads responsible for a large portion of the crashes. In Queens for example, **Northern Boulevard** and 
**Queens Boulevard** have around 100% and 50% more crashes than **Woodhaven Boulevard**. 
Unless the reader is very well versed in New Yorks street plan, the location and
names of these roads are likely unfamiliar. To better get a picture of the location and length of these roads,
the crashes for the top three dangerous roads in each borough are visualized in a map below. 

<iframe src="roadmap.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="750"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

[Map containing crashes at dangerous roads](./roadmap.html)

## Temporal distributions of the car crashes
The final set of visualizations pertaining to the raw data are the temporal developments of causes of crashes and vehicle types involved. The data is sorted by hour of the day, day of the week and months of the year, all separated into separate tabs. The contribution factors and vehicle types are selected by taken the top 14 and 11 causes of crashes, respectively. Click on the interactive legends to see how bar plots vary across hours, weeks and months.

<iframe src="Crashes_hours_weeks_months.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="1050"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

**Our observations:**
* If we sort by hours of the day, most of the violations shows the rush hour trafic pattern very clearly. For instance, for 'Driver Inattention/Distraction' the number of crashes increases between 8-9 am (morning rush hour) then drops slightly before increasing again around 4-6 pm.
* In contrast, if we look at the hourly pattern from the 'Alcohol Involvement', the inverse pattern is seen where the wee hours of the morning see the largest number of crashes (our guess is people driving home from a night out).
* We can also see that the weekly 'Alcohol Involvement' pattern sees an increase over the weekend in number of crashes, whereas 'Driver Inattention/Distraction' slightly drops over the weekend.
* Another interesting pattern is the crashes where a bicycle or a motorbike was involved. If we sort by months, we can see that this type of crash increases over the summer months (better weather means more people on bicycles/motorbikes).
* Furthermore, sorting by 'Bus' by weeks, we can see that most of the bus crashes are happening on workdays of the week, where an increased number of busses are sent in to accomodate the work-commuters.




## Machine learning 

We will now try to use all the information gathered in the previous sections to make a machine learning model for traffic injuries.  We have chosen to see if it’s possible to make a model that predict whether an injury will occur in a traffic accident. Our hypothesis is that traffic injuries don’t arise in a purely stochastic manner. It is believed their occurrence is influenced by a multitude of factors such as drivers’ physical conditions, car types, traffic condition and weather. This is based on all the interesting founding we have discovered so far. Such as the reckless young drivers, the dangerous roads and the time distributions of accidents. All these findings let us to believe this model would be possibly to do. 

No more motivation lets get to it. It might get a bit technical but hold on in. We are predicting on the “NUMBER OF INJURY” column and have transformed the column into a binary variable by combining all injuries over 0 to 1. Therefore, it has been made into a binary classification problem. 
It was showed that boroughs, time, day of the week, age, contributing factors and vehicle type all influenced traffic incidents and injuries. We therefore chose to use these features in our model. In addition to these features we also incorporated weather conditions such as temperature, humidity, wind speed and description of the weather e.g. Rain, thunder, snow and sun. 
The model we achieved the best results from was the random forest classifier from SciKit learn. With that model we achieved following results: 



![confmatrix](Confusion_ROC.png)


bla bla bla something with weather model and it didnt predict better

<iframe src="ML_feature.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

![](MLchoro.png) ![](choro_colors.PNG)

