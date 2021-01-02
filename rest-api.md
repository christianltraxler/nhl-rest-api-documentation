
# NHL REST API Documentation
---

[Franchises](#franchises)

[Countries](#countries)

[Seasons](#seasons)

[Draft](#draft)

[League Leaders](#leaders)

---
### <a name="franchises"></a>Franchises
`GET https://api.nhle.com/stats/rest/en/franchise` Returns a list of all franchises  
#### Modifiers
`?sort=fullName` Sorts the data by name (first name)  
`?include=firstSeason.id` Includes the id of the first season for the franchise  
`?include=lastSeason.id` Includes the id of the last season for the franchise (null if active)  

---
### <a name="countries"></a>Countries
`GET https://api.nhle.com/stats/rest/en/country` Returns a list of all countries  
#### Modifiers
`?sort=fullName` Sorts the data by country name  
`?include=stateProvinces` For Canada/USA, includes all states/provinces  

---
### <a name="seasons"></a>Seasons
`GET https://api.nhle.com/stats/rest/en/season` Returns a list of all seasons  
#### Modifiers
`?sort=[{"property":"id","direction":"ASC"}]` Sorts data by id (ascending)  
`?sort=[{"property":"id","direction":"DESC"}]` Sorts data by id (descending)  

---
### <a name="draft"></a>Draft
`GET https://api.nhle.com/stats/rest/en/draft` Returns a list of all drafts   
#### Modifiers
`?sort=draftyear` Sorts data by year   

---
### <a name="leaders"></a>League Leaders
`GET https://api.nhle.com/stats/rest/en/leaders/skaters/goals` Return list of top 10 most goals in any season by a player  
`GET https://api.nhle.com/stats/rest/en/leaders/skaters/assists` Return list of top 10 most assists in any season by a player  
`GET https://api.nhle.com/stats/rest/en/leaders/skaters/points`  Return list of top 10 most points in any season by a player  
`GET https://api.nhle.com/stats/rest/en/leaders/goalies/gaa` Return list of top 10 lowest goals against average (GAA) in any season by a player  
`GET https://api.nhle.com/stats/rest/en/leaders/goalies/savePctg` Return list of top 10 lowest save percentage in any season by a player  
`GET https://api.nhle.com/stats/rest/en/leaders/goalies/shutouts` Return list of top 10 most shutouts in any season by a player  

#### Modifiers
`?cayenneExp=`   
- `season=20192020` Gets data for the year specified  
- `gameType=2` Filter data based on the game type   
- `player.positionCode='D'` Filter data based on player position  
- `isRookie='Y'` Filter data based on if the player is a rookie  
- `team.franchiseId=10` Filter data based on the team  
