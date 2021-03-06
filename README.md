# Predictive-Event-Modelling

## Problem Statement
Segment the audience of a content app based on its user’s propensity to watch a video in the next 2
days

## Data 
The directory contains event details for a Video Content app. As the user engages with the app, some of 
his actions are recorded in detail. 
For example, as soon as the user launches the app, an "AppLaunched" event is recorded which contains 
details such as timestamp, os, device, country, userId etc. 
When the user registers itself for the app, a "Registered" event is raised. Similarly when he views the 
details of a video or an episode, a "VideoDetails" event is recorded. Also, when he starts watching a 
video, a "VideoStarted" event is raised. 
Many a time, app owners also engage with the customers via Push Notifications, SMS, emails etc. When 
a user clicks on any such campaign, a UTM Visited campaign is recorded. The details of all these events 
are provided below in the "Events" section. 

**Events**
The directory contains details about the following 6 events. 
1. AppLaunched 
2. AppUninstalled 
3. VideoStarted 
4. VideoDetails 
5. UTMVisited 
6. Registered 

Every event contains the following : 
1. UserId: Every app user is assigned a unique identity which is stored in this field. 
2. Date: The date on which this event was raised 
3. Minute_Of_Day: The minute of that day on which the event was raised 
4. Second: The second of the minute on which the event was raised. Date, Minute_of_Day and 
Second provides the exact timestamp of the event 
5. Country: The country Id in which the user was present while doing the event. Note that 255 
means "Unknown" country. 
6. State: The state Id of that country. For example, India will have state Ids in the range [1,29]. 
7. OS: The OS of the device from which event was raised. They are coded as : 
a. 0: Others, 1: Android, 2: iOS, 3: Windows, 4: Mac, 5: BlackBerry, 6: Linux 
8. Device: The type of device. They are coded as : 
a. 0: Desktop, 1: Mobile, 2: Tablet, 3: TV 
The events might also have some custom properties : 
1) VideoStarted and VideoDetails : 
a) Genre : The genre of the video 
b) ProgramType : Records the type - TVShow or Movie etc. 
c) Category : Records the category - Video on demand("vod") or not 
d) VideoId : The video name 
2) Registered : 
a) Status: The status of the registration 

# Evaluation Metrics: 
1. F1-score: Minimum required F1-score of 0.5 
2. Segments: Minimum of 2 segments and a maximum 4 segments can be created. 
3. Features: The goal of a marketer is to not only identify users who are likely to convert but also 
target and convert users who are unlikely to convert. Hence, the features used to create the 
model should be actionable by a marketer. 
4. Overfitting: The ability of the model to minimize overfitting and reproducing the numerical 
scores of the parameters mentioned above on the new dataset 

 
