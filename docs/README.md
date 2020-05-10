# NYC Vehicle crashes 


Since 2012 more than 1,000,000 traffic accidents have occured in New York. As a result of those accidents 200,000 people have gotten injured. Traffic incidents are therefore the leading cause of injuries in New York City. The aim of this project is to visualize, analyze and model the traffic incidents in order to find identifiable patterns that would be able to reduce the risk of injuries in New York City. 
The questions we will try to answer are; Where are the crashes happening? etc etc  


## New York through data

Test text

<iframe src="map.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>
## 

test text 

<iframe src="yearly_borough.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

##

<iframe src="Crashes_agegroups.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>



## Dangerous roads

![Drag Racing](output.png)


<iframe src="Dangerous.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="800"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

[Map containing crashes at dangerous roads](./roadmap.html)




<iframe src="Crashes_hours_weeks_months.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="1600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>


## Machine learning 
Traffic accident prediction is very difficult and requires non-accident data. It was therefore chosen to see if it was possible to predict whether an injury will occur in a traffic accident. Our hypothesis is that traffic injuries don't arise in a purely stochastic manner. It is believed their occurence is influenced by a multitude of factors such as drivers' physical conditions, car types, traffic condition and weather. 
In this section we will therefore investigate the possibility of predicting whether or not a traffic incident will involve an injury.

To do this two different machine learning models are used and tested on different feature sets. We are predicting on the "NUMBER OF INJURY" column and have transformed the column into a binary variable by combining all injuries over 0 to 1. Therefore it has been made into a binary classification problem. 


![confmatrix](confmatrix.png)

![feature](feature.png)

bla bla bla something with weather model and it didnt predict better
##

