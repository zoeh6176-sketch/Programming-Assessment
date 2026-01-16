## Programming for Data Science Summative Assessment 

Required packages:
import pandas as pd 
import glob 
import os 
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import pearsonr
import scipy.stats as stats
from scipy import stats
import numpy as np
from datetime import date 
from datetime import timedelta


Loading in Data:
From the Cricsheet website I have used a loop to read in 59 .csv files, each containing ball by ball data, from 2002 to 2025. This includes 13 Ashes test series. Each series contains 5 test matches, however, data wasn't available for the first 3 matches of the 2002/03 series and last 3 matches of the 2005 series. At first I didnt have any matches from 2005 but after emailing the person in change of the website he provided 2 of the matches for me. The matches which are missing aren't available since they have to don't have the data and to get it, have to listen to commentary radio from 2005 to get ball by ball data.

Before writing a loop I read in all the files individually. This was time consuming and not an effective way to read in so many files. I therefore quickly made the decision to use a loop instead.

Figure 1 and statistics 1: Scatter plot showing the top 15 wicket taking bowlers: strike rate vs bowling average¶
From the scatter plot and the pearson correlation you can see there is a strong positive linear correlation between bowling average and strike rate for the top 15 bowlers. The lower the bowling average and strike rate and the higher the number of wickets the better the bowler. From the scatter plot you can see Stuart Broad (English) has the most wickets. The best bowler on the plot I would argue is Mitchell Starc (Australian). He has both a low bowling average and strike rate (lower then Broad) and still a high number of wickets.

Figure 2: Bar chart of the most wickets taken between 2002 and 2025 by bowlers, excluding runouts¶
Bar chart showing the top wickets taken from all matches between 2002-2025, coloured by team of player. Stuart Broad has the most wickets and Shane Warne has the least out of the top 15. Shane Warne however has the most ashes wickets of all time with an astonishing 190 wickets. Because the 2005 dataset is incomplete Warne is missing out on a lot of wickets. In the 2005 series he took 40 wickets!

Figure 3: Heatmap showing number of dismissals by a bowler in each of the series
Heatmap shows the dominant bowlers in each series from australia and england. The heatmap however is missing the first two series since its taking the top 10 wicket takers and they didnt play in those matches. The heatmap could be inproved by distingishing australian and english players by colour of names.
The most wickets in a series was by Mitchell Johnson in the 2013/14 series. Should again be Shane Warne with 40 in 2005.

Figure 4: Bar chart of the most runs scored by batters between 2002 and 2025
Bar chart showing the top total runs from all matches between 2002-2025, coloured by team of player. Steve Smith has the most runs and Michael Hussey has the least out of the top 15. Joe Root recently took over in the most recent 2025 series.

Figure 5: Scatter plot showing the top 15 run scorers: strike rate vs batting average
Scatter plot coloured and sized by total times dismissed/ out. The higher strike rate and average runs the better. Travis Head by far has the highest strike rate.

Figure 6: Heatmap of top batters in each series¶
Heatmap showing the top runs scored in each series with Steve Smith having the most runs in the 2019 series.

Figure 7: The effect of bazball
This line plot actually shows quite a lot. The dashed line shows the progress of runs throughout an innings before the introduction of bazball and the solid is after the introduction. Each colour represents an innings. Innings 2 has the highest amount of runs as expected. After the introduction of bazball you can see the rate of runs is higher then the traditional, showing the more aggressive style of play. I also added a dotted line for when a new ball is introduced in an innings. The new ball will move around the wicket a lot more leading to a decrease in runs after the line.

Figure 8: kdeplot comparing bazball and traditional 
Shows that the run rate of bazball is higher.

Figure 9: Strike rate vs over number, how does scoring rate change as an innings progresses?¶
This scatter plot shows the mean runs per over against the over number. Shows that as an innings progresses the general trend in mean runs increases slightly. At the end of an innings the mean number of runs seems to either increase or decrease. Plot improvement: colour by innings and batting team.

Figure 10: Bar chart showing the results of matches between 2002 and 2025 (excludes first 3 matches in 2002/03 series and last 3 matches in 2005 series)¶

Figure 11: Bar chart showing the results of series

Figure 12 and statistics 3: Bar chart showing the percentage of matches won at home vs away/drawn
Hypothetically the ratio of winning at home vs away should be 50:50. In actual fact from looking at the matches from the Ashes series it's 62:38.
Home Win Rate:  62.71%
P-Value: 0.0337
Result is Statistically Significant. There is a home advantage.

Figure 13: Boxplot of distribution of match runs
Australia on average score more runs then england in a match

Figure 14: Heatmap showing head to head rivalies
Coloured by number of dismissals.

Figure 15: Bar chart of batters dissmissals by bowler and line plot how many runs they scored against that bowler

Figure 16: Percentages of types of dismissals from matches from 2002 to 2025

Figure 17: Heatmap looking at the mean number of wickets in a phase of overs in each innings
Wickets in dataframe are either 1 (indicating a wicket) or 0 (no wicket) therefore mean is between 0 and 1- the higher to 1 the more wickets.

Figure 18: Time series of 21st century ashes 
