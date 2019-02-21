# soccer

I analyze the relationship between some variables in soccer games (for example, possession versus goals scored, or fouls versus goals allowed). I also build some charts with user input that display highest scorers, highest foulers, etc for a specific European league and season.

The original data is stored in a relational database, which I query with SQL and save the data in a pandas dataframe. Becuase most of the data comes in xml format, i needed to do more extraction work on the data. I store the clean and tidy data in three different dataframes (which I then save as .csv files): 

* game_df is a dataframe that stores *game* characteristics (what teams played? how many goals for each team? how many shots on goal did each team have? etc.). 

* player_df stores data about players (how many shots on goal an individual player had? how many fouls did they commit? etc).

* goal_df stores data about goals. Although I could have stored this data in the player dataframe, I wanted to extract more information about each goal (goal time, type of goal) so joining this data with the player dataframe would have generated untidy data.

After creating these dataframes, I move on to analyzing the data. I look first at relationships between some variables, like fouls committed versus shots created per game, or team possession versus team shots per game. 

The second part of the analysis takes user input (league and season) and returns some charts about that season: who is the highest scorer? who committed the most fouls? etc. 
