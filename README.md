# spotify-pyspark

1. [Create env and install pyspark and jupyter lab](#schema1)
2. [Dataset](#schema2)
3. [Data loading  and Calculating basic statistics](#schema3)
4. [Data Cleaning](#schema4)
5. [Exploratory Data Analysis (EDA)](#schema5)
6. [Engineering Characteristics ](#schema6)
7. [Key issues to deepen Big Data analysis](#schema7)



8. [Resources](#schemaref)

<hr>
<a name='schema1'></a>

## 1. Create env and install pyspark and jupyter lab

1. Create env
```python
python3 -m venv pyspark-env
```
2. Activate
```python
source pyspark-env/bin/activate
```
3. Install Pyspark and jupyterlab
```python
pip install pyspark

pip install findspark

pip install jupyterlab
```
4. Install matplotlib and searborn
```
pip install matplotlib seaborn
```


<hr>
<a name='schema2'></a>

## 2. Dataset

- id: str, identifier of the track.
- name: str, name of the track.
- artists: str, artists of the track.
- duration_ms: float, duration of the track in milliseconds.
- release_date: date, release date of the track.
- year: int, release year of the track.
- acousticness: float, measure of acousticness of the track.
- danceability: float, measure of danceability of the track.
- energy: float, measure of energy of the track.
- instrumentalness: float, measure of instrumental elements in the track.
- liveness: float, measure of liveness of the track.
- loudness: float, loudness of the track.
- speechiness: float, measure of speechiness in the track.
- tempo: float, tempo of the track.
- valence: float, measure of valence (positivity) of the track.
- mode: int, mode of the track (major or minor).
- key: int, key of the track.
- popularity: int, popularity score of the track.
- explicit: int, indication of explicit content presence (explicit or implicit).


<hr>
<a name='schema3'></a>

## 3. Data loading  and Calculating basic statistics
- We load the dataset, with `df_schema`
- Row Counting and Unique Values
- We calculate the basic statistics.
- Analyze the null values, clean data with nulls


<hr>
<a name='schema4'></a>

## 4.  Data cleaning
- Clean and Standardize release_date
    - Extract day and month of "date_format
    - Combine year,day, month
    - Convert date_combined to yyyy-MM-dd format
- Null value analysis
- Remove Irrelevant Columns
 

<hr>
<a name='schema5'></a>

## 5. Exploratory Data Analysis (EDA)

- Descriptive Statistics
- Data Visualization with Matplotlib and Seaborn
- Correlation Map


<hr>
<a name='schema6'></a>

## 6. Engineering Characteristics 
- Creation of New Variables Based on Categories
    - Classify Tempo: Divide the tempo into categories such as slow, moderate and fast.
    - Classify Duration: Group songs by duration, such as short, medium or long.
- Scaling and Normalization of Numerical Characteristics

<hr>
<a name='schema7'></a>

## 7. Key issues to deepen Big Data analysis

- What is the average length of the most popular songs (e.g., top 10% popularity)?
- Can we observe any trends in popularity or other characteristics according to the year of release?
- What clusters of songs are formed according to 'tempo', 'valence', and 'danceability'.?
- Which artists have the highest proportion of popular songs with high 'danceability'?


<hr>
<a name='schemaref'></a>


https://www.kaggle.com/datasets/kapturovalexander/spotify-data-from-pyspark-course/data