# EPL 20-21
The following project analyzes player and team performace for the 2020/2021 English Premier League Season in the form of a Microsoft Power BI Report.

### Data Sources ###
   #### *crest_pictures.xlsx*<br> ####
   The data provides image url's for each team in the English Premier League during the 2020/2021 season, to be used for the report's slicer. 
   |Field|Description|
   |-----|-----------|
   |Team|Team Name|
   |Link|Image URL|

   #### *play_team_mappings.xlsx*<br> ####
   The data identifies the player's team at the beginning of the season using the confirmed squads listed from the [Premier League](https://www.premierleague.com/news/1869523).
   |Field|Description|
   |-----|-----------|
   |Player[^1]|Last, First Name|
   |Last Name|Last Name|
   |First Name|First Name|
   |Full Name|First, Last Name (including Middle Name)|
   |First/Last|First, Last Name (not including Middle Name)|
   |Team|Player's corresponding team|
   
   [^1]: Player transfers that occur during the season are not considered.
   
   #### *team_stats.xlsx*<br> ####
   The data provides financial, geographical, and demographical data for each team.
   |Field|Description|
   |-----|-----------|
   |Team|Team Name|
   |Stadium Location|Location of team's stadium|
   |City|City of the stadium's location|
   |Population[^2]|Number of people in the associated city|
   |Market Value[^3]|Aggregated player value|
   
   [^2]: From the UK's Official Labor Market Statistic, [nomis](https://www.nomisweb.co.uk/sources/census_2011), as of the 2011 census.
   [^3]: From [transfrmarkt](https://www.transfermarkt.us/).
   
   #### *pl_20-21.csv*<br> ####
   Individual player statistics from [Kaggle](https://www.kaggle.com/krishanthbarkav/english-premier-leagueepl-player-statistics)[^4]. Only the fields included in the analysis are listed below.
   |Field|Description|
   |-----|-----------|
   |Name|Player Name|
   |Team|Player's team|
   |Position|Player's position|
   |Appearances|Number of matches played|
   |Clean Sheets|Number of games played with no goals allowed. Only available for Goalkeepers, Defenders and Midfielders|
   |Goals Conceded|Number of goals allowed. Only available for Goalkeepers, Defenders and Midfielders|
   |Tackle success %|Number of tackles won|
   |Interceptions|Number of passes intercepted|
   |Clearances|Number of times ball is cleared outside the penalty area|
   |Recoveries|Number of times recovered behind the ball|
   |Duels won|Number of balls won against an opposing player|
   |Duels lost|Number of balls lost against an opposing player|
   |Successful 50/50s|Number of successful competitions against an opposing player|
   |Aerial battles won|Number of balls won against an opposing player in the air|
   |Aerial battles lost|Number of balls lost against an opposing player in the air|
   |Assists|Number of passes leading to a goal|
   |Passes|Number of connections with another player on the same team|
   |Big Chances created|Number of connections leading to a goal-scoring opportunity|
   |Crosses|Number of passes into an opponent's penalty area|
   |Through Balls|Number of forward passes surpassing an opponent's defender|
   |Accurate Long Balls|Number of forward passes surpassing an opponent's defender from distance|
   |Offsides|Number of times a player was beyong the last defender when the ball was passed|
   |Goals|Number of goals scored|
   |Shots on target|Number of balls shot on goal|
   |Big Chances missed|Number of times a goal was not scored given the opportunity|
   |Saves|Number of shots blocked. Only available for Goalkeepers|
  
   [^4]: Data is assumed to be accurate and complete.
   
   #### *rankings.xlsx*<br> ####
   Statistics used to calculate the most valuable player (MVP) by performance through a ranking system. Grouped by position (Goalkeeper, Defender, Midfielder, Forward), for each individual, a raw score is calculated by ranking the individuals amongst their peers for each metric and then aggregating to determine an overall score. A normalized score is then calculated to account for differences in the number of fields used and number of players in each position.  
   
   The fields used to calculate the MVP are listed in the above section. For each position, the most metric are  Additional fields and their corresponding formulas are provided below:
   |Field|Position|Description|Formula|
   |-----|--------|-----------|-------|
   |Clean Sheets per game|Goalkeeper|
   
