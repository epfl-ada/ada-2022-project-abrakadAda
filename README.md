# Wikispeedia : A glimpse of the human brain

Teva Brotherson : <br/>
Emilien Seiler : <br/>
Christophe Roger : </br>
Antoine Vincent  : <br/>

## Abstract

Wikispeedia is a game where you have to find a path between a starting article and an objective article as faster as possible by clicking on the links available on th present article. It gives a lot of informations about how a player will decide what is, according to him, the best decision to take, because the player has to make compromises between speed and reflection on what would be the optimal decision, and we want to analyze the influence of several factors on these decisions to find an eventual pattern in the human behavior through wikispeedia. <br/>
In order to do this we analyze 3 factors that could have an influence on decision-making of players : Spatial, temporal and behavioral factors that we will combine to assess the sub- optimal decisions against the engine behavior.


 - motivation : human behavior through wikispeediaco
 - story : what influe the choices of the player
 - because we think that this game gives a lot of information about the functionment of the human brain.
 - ==>GLIMPSE OF THE HUMAN BRAIN
 
## Research questions 

3 different research dimension : 
- Spatial analysis
- Behavioral analysis
- Temporal analysis
 
Those three dimensions will be useful to assess the 'sub-optimal' decisions (engine behavior)

## Proposed additional dataset
- https://www.sixdegreesofwikipedia.com/: Not properly a dataset. The algorithm of this website will serve us to find the optimal path between articles. 
	We will have to implement it locally, and implement a SQLITE database on which the algorithm can run. <br/>
	There's a whole explanation on the Github linked on how to steps to follow to use it locally (further informations on Analysis_paths.ipynb).

## Methods (chacun écrit ce qu'on fait)
- data analysis with python librairies : Pandas, Numpy, BeautifulSoup
- dataviz with Seaborn, Matplotlib

- For comportemantal analysis:
	- First, an analysis on how losing and winning influences the number of game played, using the number of games winned, lost and played to do linear regression and find the criteria that makes people want to play.
	- Secondly, the same analysis but using time spend while playing.
	- Then, an anaysis on the learning behavior of people through playing the game. I.e. if people get better the more they play the game. Need to do compaee win-rate, time spend per game, difficulty ratings... through time for each player.
	
- Concerning the analysis of the paths: 
	- Comparison of the shortest path length with the length of the paths played OK
	- Overview of the category charachteristics OK

	The following tasks consists of extracting the optimal paths and analyze the comparison with the played ones via the implementation of a local version of the above-mentioned website. 

	Another task would be to implement a hashing algorithm to find faster initial and final article and length of the paths.


## Proposed timeline
### Week 10
Path analysis:
- Setting up the local implementation of the website and mock trials.
### Week 11
Path analysis:
- Creation of the SQLITE database
- Local implementation  -> Way to find the optimal paths.
### Week 12
Path analysis:
- Comparisons between paths
- Hashing implementation
### Week 13
Path analysis:
- Extraction of the decision-making features
### Week 14
Path analysis:
- Results organisation

## Organization within the team
Christophe : Spatial data analysis, statistics and visualization <br/>
Emilien : Temporal analysis <br/>
Antoine : Behavior analysis <br/>
Teva : Players decision-making analysis <br/>

## Questions for TAs 
- We would like to incorporate machine learning into the project but we don't have ideas, where could we add some ?
