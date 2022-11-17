# Wikispeedia : A glimpse of the human brain

Teva Brotherson : <br/>
Emilien Seiler : <br/>
Christophe Roger : <br/>
Antoine Vincent  : <br/>

## Abstract

With the help of the dataset wikispeedia we will study the behavior of humans playing the game : 
 - motivation : human behavior through wikispeedia
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
https://www.sixdegreesofwikipedia.com/

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
