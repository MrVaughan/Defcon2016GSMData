# Defcon 2016 GSM Data
##WORKING DRAFT
All GSM data I collected while in Vegas at Defcon 2016. As a correction it was pointed out to me that the network I was connected to was GSM (AT&T) not CDMA . Originally I thought the phone I had was CDMA only which is why I said it was CDMA but in reality all the data is GSM.

##Overview
I was in Las Vegas from July 31st to August 7th 2016. During that time I spent 4 nights before Defcon in the Augustus Tower at Ceasars Palace (it was nice) and the following 3 nights at the Paris Hotel. Throughout the week I spent a lot of time walking around all areas of vegas while collecting GSM cell tower data using Android IMSI Catcher Detector (AIMSICD) App. https://github.com/CellularPrivacy/Android-IMSI-Catcher-Detector/wiki   

##Disclaimer
Admitadely this was a small experiment to test my curiousity and attempt to get meaningfull data to confirm or deny the hostility of the cellular networks during Defcon. Although I have done a lot of mobile application assessments and reverse engineered many mobile technologies this is my first foray into GSM, FEM2Cells, IMSI Catchers, and Stingrays. There are definitely more experts in this field and people who know way more then me. There may even be reasonable explinations for some of the abnormal behaivor observed. I wanted to get the data out quickly so that more eyes could get on it and we could draw attention to the issues. I will gladly retract or refine any observations/findings as needed, for the momment all observations should be considered preliminary.

##OpenCellID
As I continue to learn and understand the data, I've begun looking up the observed towers and Las Vegas region in OpenCellID.org I've already identified a number of GSM devices not already known to OpeCellID. One observation however is that many of the towers in my post defcon data set were already known to OpenCellID. In some locations around Las Vegas (including Paris and Bally's) there are many redundent GSM devices to continue to provide service for high traffic areas. 
In total 51 devices were identified that were not known to OpenCellID during my week in Las Vegas. This is not to say that there were 51 malicious devices but it is reasonable to assume that there may have been some malicious devices. All devices not known to OpenCellId are located in the Towers_Not_In_OpenCellID.org.csv file. More analysis on this data is avaible in the observations section.

##Coverage
Before Defcon I made multiple walks of Paris and Bally's to get a baseline list of the available towers in the area.I did make a trip to Blackhat for a day to check out the expo floor. In addition to many walks of the strip and my wife's love of going in all the shops, our company also did a limo tour of the strip and had a nice team dinner at Wynn. Over the course of the week minus some occassions where the app crashed I feel I have pretty reasonable coverage of most of the vegas strip.

##About IMSI Catchers/Stingrays
more to add

##Data
All data is available in the BaseTransceiverStation.csv file. Feel free to slip this over to an open map interface for me. Bonus points if you can plot my travel path.

##Observations

###Paris and Bally's Pre Walk

In my pre-conference walk I walked the casino floors and the conference areas I could get into. I was not able to get into the contest area in ballys or the speaker rooms. I also walked most of the exterior of the casinos. I did not go beyond the main level. It is conceivable that the hotel has multiple tower device on multiple floors which would explain some of the additional data points on the later image but I'm not convinced this is consistent with what I was observing with other hotels I was in that week.

The image shows the towers captured during preliminary war walks of Paris and Bally's

![](https://github.com/MrVaughan/Defcon2016CDMAData/blob/master/images/Screenshot_2016-08-03-23-36-37_Pre_Defcon_Paris_Ballys.png?raw=true)

###Paris and Bally's Post Defcon

Once I checked into Paris I continued to collect data throughout Defcon. The observations show significant increase in the number of towers in there area. There are a couple potential 'reasonable' explanations (like maybe there are towers on multiple floors throughout the building) but at the least I think it is reasonable to conclude that there were at least a few malicious GSM devices at the conference.

This image shows towers captured between August 4th and 7th at Paris and Bally's

![](https://github.com/MrVaughan/Defcon2016CDMAData/blob/master/images/Screenshot_2016-08-07-14-18-58_Post%20Defcon.png?raw=true)

Once I had a chance to look at the data I could determine all the devices not already known to OpenCellId. In total 51 devices were identified in Las Vegas that were not already known to OpenCellID. This is not to say that there are 51 malicious devices however it is a high non-zero number that leads to the possibility that there were malicious devices in the region. Bellow is an image of the uknown devices identified around Paris and Bally's. In total there were 14 previously unreported devices around these two hotels. 

![](https://github.com/MrVaughan/Defcon2016GSMData/blob/master/images/Paris_Ballys_Unknown_Devices.png?raw=true)

###Caesar's Main floor

I wanted to provide a sense for what mostly presumed normal data would look like. Throughout the first 4 days of my trip I spent a lot of time walking around the Caesar's lobby, shops and casino. This data does not show any obvious malicious towers or any accessive number of towers.

![](https://github.com/MrVaughan/Defcon2016CDMAData/blob/master/images/Screenshot_2016-08-09-11-40-45_Normal%20Area.png?raw=true)

###Augustus Tower

While staying in Caesars before Defcon I was seeing all sorts of malicious activity just sitting in my room. The room was located in the Augustus Tower. This image shows all the towers that my phone picked up mostly just sitting in the room. This suggest that there were devices either driving by or flying overhead throughout the days prior to defcon (and while Blackhat and BSides Las Vegas were going on).

![](https://github.com/MrVaughan/Defcon2016CDMAData/blob/master/images/Screenshot_2016-08-09-11-28-38_Augustus%20Tower.png?raw=true)

When I considered these observations with devices not known to OpenCellId the following 4 devices were revealed in the area outside my hotel room at Caesar's. This is not confirmation that there were malicous devices outside my hotel but suggests strongly that some suspicious activity was occuring. 

~[](https://github.com/MrVaughan/Defcon2016GSMData/blob/master/images/Hamstermaps_Not_In_Opencellid_Caesars.png?raw=true)

###Abnormal Tower 1
The day I left defcon I sat on the airplane for 4 hours (with no A/C, thanks for that Air Canada). My cell phone was caught by an unusual tower. 

|mobileCountryCode|mobileNetworkCode|locationAreaCode|cellId|primaryScramblingCode|timeFirst|timeLast|gpsLat|gpsLong|TimesSceneInOpencellID
|---|---|---|---|---|---|---|---|---|---|
|310|410|33800|92181001|2147483647|2016-08-07 21:27:16 +0000|2016-08-07 22:39:56 +0000|36.08274891|-115.1347721|77

What is interesting and unusual about this device is that OpenCellID users have reported seeing this device an overwhelming ~77 times in another location over 4 miles away. What was it doing at the airport during Defcon Sunday?

Here is where I found this tower:
![](https://github.com/MrVaughan/Defcon2016GSMData/blob/master/images/WeirdTowerA.png?raw=true)

Here is where OpenCellID users mostly reported seing this tower:
![](https://github.com/MrVaughan/Defcon2016GSMData/blob/master/images/WeirdTowerA_OpenCellID.png?raw=true)

Here you can see the distance between where OpenCellID users have scene the tower and the airport:
![](https://github.com/MrVaughan/Defcon2016GSMData/blob/master/images/WeirdTowerA_Distance.png?raw=true)


This raises a number of questions. The first obvious one: What reasonable explanation could there be for this tower to be in another location or for my phone to pick it up from such distance? It seems there were hundreds of towers closer then this one my phone could have connected to. Is this just a really high strength actual tower (most of the ones in the casinos are probably more like large routers) or did it move? If this is a malicous device, what companies opperate in the "home location" address of this device?

###LTS to 3G downgrade attacks
This was happening all the time especially during my stay in the above listed Augustus Tower. More info to add.

###Defenses
will add

###To Do
* Going to separate all the data sets so we can start to build lists of known good/bad towers. If others in vegas can contribute or on future trips we can confirm permanent (potentially good) devices vs temporary devices.
* Export all data to a maps api or something

##Open questions?
* Is this unique to Defcon and the many security conferences happening that week in vegas or would activities like the drive by captures I experienced still occur regardless of the conferences?
* Wouldn't it be nice if we could tell people defcon was the safest time to use your equipement in vegas thanks to all the hackers of the world?
* Certainly a burner phone was worth it but what about the thousands of innocent regular people in the area that week?
* Impact of GPS accuracy?
* Could Towers be rotating or changing device ID's resulting in duplicate entries?
