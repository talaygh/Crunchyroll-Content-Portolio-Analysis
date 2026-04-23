# Crunchyroll-Content-Portolio-Analysis
End-to-end analytics portfolio project | Snowflake · SQL · Tableau · Snowflake Cortex AI

Crunchyroll Content Portfolio Analysis
End-to-end analytics portfolio project | Snowflake · SQL · Tableau · Snowflake Cortex AI

Overview
A self-initiated portfolio project analyzing Crunchyroll's anime content library across 1,400+ titles. Built to demonstrate a full analytics pipeline — from raw data ingestion to executive-level dashboard delivery — targeting a Finance Data Analyst use case focused on content performance, audience demand, and investment signals.
Live Dashboard: View on Tableau Public

Tech Stack
LayerToolData SourceKaggle (anime dataset)Data WarehouseSnowflakeTransformationSQL (Snowflake)Sentiment AnalysisSnowflake Cortex AIVisualizationTableau Public

Dashboard Views

Genre Performance — Engagement and rating scores across 20 genres
Catalog Trend — Release volume and ratings by decade
Demand Distribution — Top 10% of titles drive 86% of audience demand
Sentiment vs Rating — Cortex AI sentiment scores plotted against IMDb ratings
Talent Tiers — Top 50 voice actors ranked by catalog presence
Genre Combos — Co-genre performance matrix (e.g. action+thriller, drama+romance)


Data & Methodology

Source data loaded into Snowflake via staged CSV files
SQL transformations used to build aggregated views per genre, decade, demand decile, and talent
Snowflake Cortex AI used for sentiment scoring on title descriptions
Some fields (e.g. IMDb votes, season counts) contain nulls in the source — these were excluded at query time rather than imputed, as imputation would introduce noise into engagement and rating averages
Final outputs exported as CSVs and connected to Tableau


Key Insights

Documentation and Western genres lead in average engagement despite low title counts
Top 10% of titles by popularity account for ~86% of total audience demand
Sentiment scores show weak positive correlation with IMDb ratings — highly-rated titles aren't always positively described
Drama+Thriller is the highest-volume genre combination; Horror+Romance is the rarest


Files
FileDescriptionCrunchyroll.twbxPackaged Tableau workbook (includes all data)Crunchyroll_Genre.csvGenre-level aggregatesCrunchyroll_Sentiment.csvCortex AI sentiment scoresCrunchyroll_Demand.csvDemand decile distributionCrunchyroll_Talent.csvVoice actor rankingsCrunchyroll_Decade.csvRelease trends by decadeCrunchyroll_GenreCombos.csvCo-genre matrix
