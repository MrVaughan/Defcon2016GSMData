# Defcon2016CDMAData
Just a place to dump the cdma data I collected while at Defcon 2016

##Overview
I was in Las Vegas from July 31st to August 7th 2016. During that time I spent 4 nights before Defcon in the Augustus Tower at Ceasars Palace (it was nice) and the following 3 nights at Paris. Throughout the week I spent a lot of time walking around all areas of vegas while collecting CDMA cell tower data using Android IMSI Catcher Detector (AIMSICD) App. https://github.com/CellularPrivacy/Android-IMSI-Catcher-Detector/wiki   

#Coverage
Before Defcon I made multiple walks of Paris and Bally's to get a baseline list of the available towers in the area.I did make a trip to Blackhat for a day to check out the expo floor. In addition to many walks of the strip and my wife's love of going in all the shops, our company also did a limo tour of the strip and had a nice team dinner at Wynn. Over the course of the week minus some occassions where the app crashed I feel I have pretty reasonable coverage of most of the vegas strip.

##About IMSI Catchers/Stingrays
more to add

##Data
All data is available in the BaseTransceiverStation.csv file.

##Observations

###Paris and Bally's Pre Walk

In my pre-conference walk I walked the casino floors and the conference areas I could get into. I was not able to get into the contest area in ballys or the speaker rooms. I also walked most of the exterior of the casinos. I did not go beyond the main level. It is conceivable that the hotel has multiple tower device on multiple floors which would explain some of the additional data points on the later graphs but I'm not convinced this is consistent with what I was observing with other hotels I was in that week.

The image shows the towers captured during preliminary war walks of Paris and Bally's

![](https://github.com/MrVaughan/Defcon2016CDMAData/blob/master/images/Screenshot_2016-08-03-23-36-37_Pre_Defcon_Paris_Ballys.png?raw=true)

###Paris and Bally's Post Defcon

Once I checked into Paris I continued to collect data throughout Defcon. The observations show significant increase in the number of towers in there area. There are a couple potential 'reasonable' explanations (like maybe there are towers on multiple floors throughout the building) but at the least I think it is reasonable to conclude that there were at least a few malicious CDMA devices at the conference.

This image shows towers captured between August 4th and 7th at Paris and Bally's

![](https://github.com/MrVaughan/Defcon2016CDMAData/blob/master/images/Screenshot_2016-08-07-14-18-58_Post%20Defcon.png?raw=true)


###Caesar's Main floor

I wanted to provide a sense for what mostly presumed normal data would look like. Throughout the first 4 days of my trip I spent a lot of time walking around the Caesar's lobby, shops and casino. This data does not show any obvious malicious towers or any accessive number of towers.

![](https://github.com/MrVaughan/Defcon2016CDMAData/blob/master/images/Screenshot_2016-08-09-11-40-45_Normal%20Area.png?raw=true)

###Augustus Tower

While staying in Caesars before Defcon I was seeing all sorts of malicious activity just sitting in my room. The room was located in the Augustus Tower. This image shows all the towers that my phone picked up mostly just sitting in the room. This suggest that there were devices either driving by or flying overhead throughout the days prior to defcon (and while Blackhat and BSides Las Vegas were going on).

![](https://github.com/MrVaughan/Defcon2016CDMAData/blob/master/images/Screenshot_2016-08-09-11-28-38_Augustus%20Tower.png?raw=true)

###LTS to 3G downgrade attacks
This was happening all the time especially during my stay in the above listed Augustus Tower. More info to add.

###Defenses
will add

###To Do
Going to separate all the data sets so we can start to build lists of known good/bad towers. If others in vegas can contribute or on future trips we can confirm permanent (potentially good) devices vs temporary devices.

##Open questions?
* Is this unique to Defcon and the many security conferences happening that week in vegas or would activities like the drive by captures I experienced still occur regardless of the conferences?
* Wouldn't it be nice if we could tell people defcon was the safest time to use your equipement in vegas thanks to all the hackers of the world?
* Was a burner phone worth it? What about the thousands of innocent regular people in the area that week?
