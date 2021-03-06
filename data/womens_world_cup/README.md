# Women's World Cup 

Data for the Women's World Cup

Source: https://data.world/sportsvizsunday/womens-world-cup-data/workspace

## Womens Squads

Data from the Womens Squad.xlsx file

### 2019 Players 

Players in the 2019 Women's World Cup. 

Header | Definition 
--- | ------
`Squad no.` | jersey number 
`Country` | country name 
`Pos.` | player position 
`Player` | player name 
`DOB` | date of birth 
`Age` | age
`Caps` |  number of games played at the international level 
`Goals` | number of goals 
`Club` | club soccer team name 


### Top Appearances 

Players who have appeared in the most Women's World Cups. 

Header | Definition 
--- | ------
`Team` | country name 
`Player` | player name
`Matches` | number of matches played in World Cups 
`Tournamets` | years player has played in the World Cup 


### Performance 

How well countries have done in the Women's World Cup. 

Header | Definition 
--- | ------
`Team` | country name 
`1991-2019` | How far the country progressed in the World Cup 


### Rankings

Country rankings. 

Header | Definition 
--- | ------
`Rank` | country rank in women's soccer 
`Team` | country name 
`Part` | ????
`Pld` | ????
`W` | wins 
`D` | draws
`L` | losses 
`GF`| goals for
`GA` | goals against 
`GD` | goal differentials 
`Points` | points 


### Hosts

Information about World Cup host countries. 

Header | Definition 
--- | ------
`Year` | World Cup year 
`Host` | name of host country 
`Matches` | number of matches hosted in the tournament 
`Teams` | number of teams in the tournament 
`Total Attendance` | number of people who attended games 
`Max Attendance` | maximum possible attendance for the tournament 


## FIFA Womens' World Cup Results 

Results from the Women's World Cups. 

Header | Definition 
--- | ------
`Year` | year 
`Team 1` | 3 letter code for country 1 name 
`Score 1` | score for team 1 
`Team 2` | 3 letter code for country 2 name 
`Score 2` | score for team 2 
`Round` | game round 

## world_cup_2019.json

Source: https://worldcup.sfg.io/matches

This is a JSON file so it's a little different than the others. You can learn more about JSON files [here].(https://www.w3schools.com/whatis/whatis_json.asp)

This dataset contains information on each game from the 2019 Women's World Cup including information about the venue, location, attendance, officials, winner, goals, substitutions, fouls, weather, attempts on goal and whether they were on or off target, corners, offside, pass accuracy and count, ball possession, distance covered, tackles, clearances, yellow and red cards, tactics, starting eleven and substitutes, 

To use this data in R, you can run the following code:

```
# load library to parse json file (you may have to install this)
library(jsonlite)

# read in data
wc_stats <- read_json('world_cup_2019.json', 
  simplifyDataFrame = TRUE, simplifyVector = TRUE, flatten = TRUE)
```

Note that this dataframe is a little more complicated than what we're used to because in some cells there are actually other dataframes! So some of this might be a bit more challenging to parse. 
