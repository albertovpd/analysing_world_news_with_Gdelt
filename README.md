# Analysing world news with the Gdelt Project. 

Here I will be attaching all my Gdelt-related leisure projects. The list of projects briefly involves:
- Used tools and languages.
- Dashboard url.
- Repository url.
- Preview of each project (after the list).

The only one weekly automated is the first one (once I know by heart how to do it, there is no point on replicating it), nevertheless you can find instructions to automate the updates in all of them.

----------------------------------------------

**1. Socioeconomic Portrait Project.** 

- Automated ETL in Google Cloud Platform weekly updated, dashboarding.
- Python, SQL.
- Bigquery and the Gdelt Project.
- Dashboard => https://datastudio.google.com/reporting/755f3183-dd44-4073-804e-9f7d3d993315
- Repository => https://github.com/albertovpd/automated_etl_google_cloud-social_dashboard

**2. Elon Musk influence in world news.**

- SQL, Bigquery, the Gdelt Project, dashboarding.
- Dashboard => https://datastudio.google.com/u/0/reporting/4578bcda-00a9-46e5-aacc-d773bfb360c2
- Repository => https://github.com/albertovpd/elon_musk_influence_in_news


**3. Monitoring unemployment in Spain.**

I really like this one. It is the most visual, it tells a story, and sources that feed the graphs are shown, you can navigate through them.

- SQL, Bigquery, the Gdelt Project, dashboarding.
- Dashboard => https://datastudio.google.com/u/1/reporting/a038e53e-ba0d-49a6-b8c9-6893445cc54a/page/UVSZB
- Repository => https://github.com/albertovpd/monitoring_unemployment


**4. Controversial public figures with Gdelt.**

- SQL, Bigquery, the Gdelt Project, dashboarding.
- Dashboard => https://datastudio.google.com/s/nShAIQD96fc
- Repository => https://github.com/albertovpd/analysing_controversial_public_figures_gdelt






--------------------------

# Socioeconomic Portrait Project. A Google Cloud ETL.

<details>
  <summary>Click to expand</summary>

Is there a way of monitoring some aspects of the global crisis in Spain? I believe so, and this is the motivation to develop this automated **ETL** process in **Google Cloud** involving **Google Trends**, sentiment analysis and influence in news through **the Gdelt Project** and **Twitter**, from raw data acquisition to the final dashboard. Thanks to it, I have been fighting with credentials, permissions, storage locations, processing locations, 3rd party authentications, Cloud Functions, pipelines, trigger schedulers with different time format, Dataprep global updates, etc... And I learned a lot in the way, quaratine fun! :D

- Tools:
    - Cloud Function with Python script: Google Trends API
    - Weekly activated with Cloud Scheduler through Pub/Sub
    - Overwriting weekly a Cloud Storage file
    - Periodically appended to BigQuery with Dataprep
    - Modified with BigQuery and stored in different tables
    - Enriched with BigQuery through the Gdelt Project dataset
    - Visualized with Data Studio

- Dashboard => https://datastudio.google.com/reporting/755f3183-dd44-4073-804e-9f7d3d993315

- Repository => https://github.com/albertovpd/automated_etl_google_cloud-social_dashboard

It is worth mentioning the selector buttons are there just to have a clear picture of graphs. With them you can select the curves you want.
![alt](pics/socioeconomic_project.png)

</details>

---------------------------------

# Elon Musk influence in world news:

<details>
  <summary>Click to expand</summary>

What the world media say about Elon Musk or his companies? That is the sentiment associated to his related news? What were the most positive and negative articles ever written about him? Let's check it out.

It has been really interesting to discover that "cheap clickbait webpages" are the ones mentioning more often Mr. Musk, even more than his own webpages like "teslamotors" or similar. In the end, he is a controversial public figure with always a really personal point of view.

Also interesting is the fact that the webpages I was expecting to see appears from under the 22th position, like *Forbes*, *New York Times*.

- Dashboard => https://datastudio.google.com/u/0/reporting/4578bcda-00a9-46e5-aacc-d773bfb360c2

- Repository => https://github.com/albertovpd/elon_musk_influence_in_news

![alt](pics/elon_project.png)

</details>

-----------------------------


# Monitoring Unemployment

<details>
  <summary>Click to expand</summary>

Everyone is afraid right now of a Global crisis like in 2008. Can we check how often is mentioned in national press unemployment-related topics, and compare nowadays results with the 2008 ones?

The answer: Yes
If we also want to check the involved articles: Just from 2015.


- Dashboard => https://datastudio.google.com/u/1/reporting/a038e53e-ba0d-49a6-b8c9-6893445cc54a/page/UVSZB

- Repository => https://github.com/albertovpd/monitoring_unemployment

![alt](pics/unemployment.png)

</details>

------------

# Controversial public figures with Gdelt:

<details>
  <summary>Click to expand</summary>

I like reading "alternative" sources, like reddit, *hackernews* or *meneame*, and once in a while I read some news about delicate matters involving the King Emeritus of Spain. This articles always express a deep frustration about how this news are not being published in his country.

So, the questions I am trying to answer are the following: 

Are the spanish news not publishing the same than the rest of world about the King Emeritus of Spain?

Do we have a method to impartially contrast it?

- Dashboard => https://datastudio.google.com/s/nShAIQD96fc

- Repository => https://github.com/albertovpd/analysing_controversial_public_figures_gdelt

![alt](pics/controversial_project.png)

</details>

----------------------------------------
------------


Alberto Vargas. 
- **https://www.linkedin.com/in/alberto-vargas-pina/**