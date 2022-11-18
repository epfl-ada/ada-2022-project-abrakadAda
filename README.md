# Wikispeedia : A glimpse of the human brain

Teva Brotherson : <br/>
Emilien Seiler : <br/>
Christophe Roger : </br>
Antoine Vincent  : <br/>

## Abstract

Wikispeedia is a game where you have to find a path between a starting article and an objective article as faster as possible by clicking on the links available on th present article. It gives a lot of informations about how a player will decide what is, according to him, the best decision to take, because the player has to make compromises between speed and reflection on what would be the optimal decision, and we want to analyze the influence of several factors on these decisions to find an eventual pattern in the human behavior through wikispeedia. <br/>
In order to do this we analyze 3 factors that could have an influence on decision-making of players : Spatial, temporal and behavioral factors that we will combine to assess the sub- optimal decisions against the engine behavior.
 
## Research questions 
3 different research dimension : 
### Spatial analysis : 
Does the location of the links in the wikipedia article have an influence on the decisions of the players ? <br/>
Does the average difference between the location of the clicked link and the best link is significant ? <br/>

Resources : 

- Dimitar Dimitrov, Philipp Singer, Florian Lemmerich, and Markus Strohmaier. 2017. What Makes a Link Successful on Wikipedia? In Proceedings of the 26th International Conference on World Wide Web (WWW '17). International World Wide Web Conferences Steering Committee, Republic and Canton of Geneva, CHE, 917–926. https://doi.org/10.1145/3038912.3052613
- D. Dimitrov, P. Singer, F. Lemmerich, and M. Strohmaier. Visual positions of links and clicks on wikipedia. In Int. Conference Companion on World Wide Web, 2016. 
- D. Lamprecht, K. Lerman, D. Helic, and M. Strohmaier. How the structure of wikipedia articles influences user navigation. New Review of Hypermedia and Multimedia, pages 1--22, 2016

### Behavioral analysis


### Temporal analysis
Are the players infulenced by the mainstream topics of the period in which they play ? <br/>
Do the "mainstream" topics stay in the reader's mind ? <br/>
Do 2 players of a game with the same conditions play differently if they play at a different time ? <br/>

And we combine those three axis to assess the 'sub-optimal' decisions against what would be the optimal decisions.

## Proposed additional dataset
- https://www.sixdegreesofwikipedia.com/: Not properly a dataset. The algorithm of this website will serve us to find the optimal path between articles. 
	We will have to implement it locally, and implement a SQLITE database on which the algorithm can run. <br/>
	There's a whole explanation on the Github linked on how to steps to follow to use it locally (further informations on Analysis_paths.ipynb).

## Methods (chacun écrit ce qu'on fait)
- For spatial analysis : 
	- First parse the html version of every articles to extract the available links on each page and their position in the page with the library BeautifulSoup
	- Then, by analyzing the finished and unfinished paths, assessing the positions of links clicked
	- Finally, if possible, analyzing the position differences between the links clicked and the optimal links.
- For behavioral analysis:
	- First, an analysis on how losing and winning influences the number of game played, using the number of games winned, lost and played to do linear regression and find the criteria that makes people want to play.
	- Secondly, the same analysis but using time spend while playing.
	- Then, an anaysis on the learning behavior of people through playing the game. I.e. if people get better the more they play the game. Need to do compaee win-rate, time spend per game, difficulty ratings... through time for each player.
- For temporal analysis:
	- Extract data to extract the precise time of each path.
	- Extract all topics from each path
	- Extract the most used topics in each month
	- Create a dataset of consumer events for each month (August 2008 to January 2014) and label them with the same set of labels as the article topics. I will use the wikipedia page of each month to create the dataset. (ex : https://en.wikipedia.org/wiki/Portal:Current_events/August_2014)
	- Perform statistical tests to see if there are redundancies with the main topics of each month
- Concerning the analysis of the paths: 
	- Comparison of the shortest path length with the length of the paths played OK
	- Overview of the category charachteristics OK

	The following tasks consists of extracting the optimal paths and analyze the comparison with the played ones via the implementation of a local version of the above-mentioned website. 

	Another task would be to implement a hashing algorithm to find faster initial and final article and length of the paths.


## Proposed timeline
### Week 
Temporal analysis: 
- End of data wrangling + start create dataset <br/>
Path analysis:
- Setting up the local implementation of the website and mock trials.
### Week 11
-Temporal analysis: 
	- Dataset creation <br/>
-Path analysis:
	- Creation of the SQLITE database
	- Local implementation  -> Way to find the optimal paths.
### Week 12
Temporal analysis: 
- Statistical analysis -> first result <br/>
Path analysis:
- Comparisons between paths
- Hashing implementation
### Week 13
Temporal analysis: 
- Shuffle result with other part <br/>
Path analysis:
- Extraction of the decision-making features
### Week 14
Temporal analysis: 
- Result organisation <br/>
Path analysis:
- Results organisation

## Organization within the team
Christophe : Spatial data analysis, statistics and visualization <br/>
Emilien : Temporal analysis <br/>
Antoine : Behavior analysis <br/>
Teva : Players decision-making analysis <br/>

## Questions for TAs 
- Do we know where the players are coming from (to select the right main event)  <br/>
- We would like to incorporate machine learning into the project but we don't have ideas, where could we add some ?
