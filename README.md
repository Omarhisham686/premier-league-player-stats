# premier-league-player-stats

## table of content:
- [project overview](#project-overview)
- [data source](#data-source)
- [tools](#tools)
- [data cleaning and perpration](#data-cleaning-and-perpration)
- [exploatary data analysis (EDA)](#exploatary-data-analysis (EDA))
- [data analysis](#data-analysis)
- [results](#results)

### project overview

Built an end-to-end data analytics project using SQL and Power BI to analyze Premier League player performance.

- Extracted and cleaned data using SQL

- Designed data models for efficient analysis

- Built interactive Power BI dashboards to visualize key metrics (goals, assists, performance trends)

The project helped uncover insights into player performance across seasons

### data source

"the primary data set used for this analysis is the "epl_player_stats_24_25.csv"

### tools
- sql server (data cleaning)
- powerbi (dashboard)

### data cleaning/perepration
in the data prepration phase we performed :
- data loading and inspection
- handling mising values
- data cleaning

### exploatary data analysis (EDA)
EDA involve explore the data to answer key question such as:

1- as a goalkeeper who has the most saves and most clean sheets

2- as a defender who has the most interseption and tackels

3- as a middfilder who has the most assists and passes

4- as forward who scored the most goals

### data analysis
Include some code worked with:
``` dax
Top_Attacker_Goals = 
MAXX (
    TOPN (
        1,
        FILTER (
            'epl_player_stats_24_25',
            'epl_player_stats_24_25'[Position] = "fwd"
        ),
        'epl_player_stats_24_25'[Goals], DESC
    ),
    'epl_player_stats_24_25'[Goals]
)
```
### results 
the result summarized as follow:

we analyized each player based on his statistics to determine who performed well and benefited their team, and who performed poorly and was a burden.
