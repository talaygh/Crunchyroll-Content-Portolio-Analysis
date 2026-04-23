# Crunchyroll Content Portfolio Analysis
## End-to-end analytics portfolio project | Snowflake · SQL · Tableau · Snowflake Cortex AI

## Overview
A self-initiated portfolio project analyzing Crunchyroll's anime content library across 1,400+ titles. Built to demonstrate a full analytics pipeline — from raw data ingestion to executive-level dashboard delivery — targeting a Finance Data Analyst use case focused on content performance, audience demand, and investment signals.
Live Dashboard: View on Tableau Public

## Tech Stack
LayerToolData SourceKaggleData WarehouseSnowflakeTransformationSQL (Snowflake)Sentiment AnalysisSnowflake Cortex AIVisualizationTableau Public

## Dataset
Downloaded from Kaggle: Crunchyroll Animes and Movies by victorsoeiro.
Two source files:

titles.csv — 1,400+ titles with IMDb/TMDB scores, genres, release year, runtime, seasons
credits.csv — 9,900+ actor and director credits joinable to titles via id

Both files were staged and loaded into Snowflake for transformation and analysis.

Dashboard Views

Genre Performance — Engagement and rating scores across 20 genres
Catalog Trend — Release volume and ratings by decade
Demand Distribution — Top 10% of titles drive 86% of audience demand
Sentiment vs Rating — Cortex AI sentiment scores plotted against IMDb ratings
Talent Tiers — Top 50 voice actors ranked by catalog presence
Genre Combos — Co-genre performance matrix (e.g. action+thriller, drama+romance)


Methodology

Raw CSVs staged and loaded into Snowflake (RAW schema)
SQL transformations built aggregated views per genre, decade, demand decile, and talent
Genre column was stored as a raw array string — parsed and flattened using Snowflake's LATERAL FLATTEN
Snowflake Cortex AI used for sentiment scoring on title descriptions
Some fields (e.g. IMDb votes, season counts) contain nulls in the source — excluded at query time rather than imputed to avoid noise in averages
Final outputs exported as CSVs and visualized in Tableau Public


Key Insights

Documentation and Western genres lead in average engagement despite low title counts
Top 10% of titles by popularity account for ~86% of total audience demand
Sentiment scores show weak positive correlation with IMDb ratings
Drama+Thriller is the highest-volume genre combination


Files
FileDescriptionCrunchyroll.twbxPackaged Tableau workbook (includes all data)titles.csvRaw source — title metadata from Kagglecredits.csvRaw source — actor/director credits from KaggleCrunchyroll_Genre.csvGenre-level aggregatesCrunchyroll_Sentiment.csvCortex AI sentiment scoresCrunchyroll_Demand.csvDemand decile distributionCrunchyroll_Talent.csvVoice actor rankingsCrunchyroll_Decade.csvRelease trends by decadeCrunchyroll_GenreCombos.csvCo-genre matrix

Author
Talay Kamali — Data Analyst
Tableau Public Profile
