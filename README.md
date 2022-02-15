# Nigeria_ACLED-DataVizualization
This is an exploratory data analysis on Newsfeed and ACLED Data of Nigeria in 2019. I have created interactive visualizations using the pandas-bokeh library and used NLP techniques to correlate events to words in news descriptions

<img width="259" alt="image" src="https://user-images.githubusercontent.com/67541365/154088663-5f0ea4c5-f4c1-4093-ba21-b9e221b1044b.png">
* Fatalities for each month and what caused them: It is seen that total fatalities were greater than 500 in the months of February to June 2019 post which the fatality numbers taper down to a little over 300 in December 2019. Moreover, for any given month the bulk of the fatalities are found to be due to Battles or Violence against Civilians.

<img width="265" alt="image" src="https://user-images.githubusercontent.com/67541365/154088813-0417f3cd-3024-4525-82cc-538355f056cb.png">
*  If we were to prioritize ‘Violence against Civilians’ as a key metric for peace keeping, we find that the monthly trend in violent acts peaks in February and tapers of drastically from 119 in February to 44 in December.

<img width="259" alt="image" src="https://user-images.githubusercontent.com/67541365/154088987-5edcf55a-ff29-4809-aff2-995dda494621.png">
* On investigating further about the fatalities of civilians due to each of these events, we notice that greater than 100 people died due to ‘violence against civilians (VAC)’ acts from January to July 2019. Also note that January had the least number of VAC events (i.e. 37) but still led to 118 deaths and March with 70 such events had the most deaths (i.e. 332)

<img width="370" alt="image" src="https://user-images.githubusercontent.com/67541365/154089124-db9a3c89-fe7e-4fa3-8d00-281f81180f7a.png">
* Now we must know who the main named actors behind these violent acts against civilians are. We see that Unidentified armed groups Nigeria (310 events), followed by Fulani Ethnic Militia Nigeria (102 events) led to most events.

<img width="277" alt="image" src="https://user-images.githubusercontent.com/67541365/154089227-c147893c-90ad-4699-ad89-8532e377c79c.png">
*	We can also use the same count methodology for each location in Nigeria to assess safety in places. We notice that out of the 947 locations in dataset the top 25 unsafe ones are shown below. Note that most places had such VAC events once in 2019.

Data was analyzed using the ‘pandas’ library in Python3 and interactive visualization was created using pandas-bokeh library. The goal was to investigate the safety of civilians in Nigeria in 2019 and identify monthly trend in violent acts, fatalities and understand what type of events have occurred around the year. Post this, the focus was on investigating the locations and named actors in these events to identify reasons for occurrence. Violent acts against civilians occurred time and again in the 25 worst cities shown above and are indicative of the lack of corrective action on part of law enforcement. The key actors are also listed above but the fact that most VAC event actors are Unidentified Armed Groups may be alarming.

# NLP on Newsfeed Data
<img width="292" alt="image" src="https://user-images.githubusercontent.com/67541365/154089608-93cd35d5-3fef-483d-99c0-3cfa94645ea3.png">
* A looming question was also the likelihood of a news source showing a particular incident type. I noticed a large imbalance in the dataset with most articles being sourced at EMM while On Watch and Security Monitor are sources for fewer events. This may be because of the large presence of the incident types that EMM reports about in given data. The other 2 news sources i.e. Risk advisory and Intelligence reports show null values in incident type records. We also notice that ‘Armed Conflict’ was sourced only at the Security Monitor and each source offers a unique incident type in articles. We further notice that there are no common incident types amongst sources. 

## Word Cloud for Article Descriptions and 3-grams
<img width="206" alt="image" src="https://user-images.githubusercontent.com/67541365/154089832-befb2947-cb70-4a89-b579-35eb204b1584.png">
<img width="229" alt="image" src="https://user-images.githubusercontent.com/67541365/154089913-4e2a2304-be27-4550-b008-317a35b7d416.png">

On cleaning, plotting n grams and collecting all the text in the short and long descriptions, we find that kill, attack, haram, ago and min are the most frequently used words by news sources in short descriptions as seen in word cloud below. Furthermore, the most common bigrams in the text are ‘min ago’ and ‘boko haram’. This is indicative of the fact that many events have something to do with the terrorist organization. Other common words include Sri Lanka, haram attack, build collapse, gunmen kill which give us more insight into the gruesome nature of events. On studying the 3 grams we see that the ‘news min ago’ is a common phrase in the description which shows that there may be little lag between news being received by the source and it being published on their websites. 
 I also extracted features from each short description (as unigrams and bigrams) using TFIDF Vectorizer to correlate with the type of incident as shown below. Governance related events involve race (politicical), crackdowns (of terrorist actors), inspection (of events) and overturning (existing authorities). With bigrams we see that often Governance related events have something to do with elections, media bills, the Nigerian President and Buhari (a retired Nigerian Army Major General). In this manner we can tie a rough outline around each Incident type and know of its nature as revealed by n grams:
for e.g. 
* Description Category 'Governance':

Most correlated unigrams:
	. crackdown, race, intensify, overturn, inspect
	
Most correlated bigrams:
	. nigeria elect, media bill, main opposite, nigeria Buhari, nigeria presid

# To be continued




