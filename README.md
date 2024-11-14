# spotify-pyspark

1. [Create env and install pyspark and jupyter lab](#schema1)
2. [Dataset](#schema2)
3. [Data loading  and Calculating basic statistics](#schema3)


4. [Exploratory Data Analysis (EDA)](#schema4)
5. [Clustering with MLlib in PySpark (K-means)](#schema5)
6. [Conclusion](#schema6)
7. [Resources](#schemaref)

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


## 4.  Data cleaning
- Clean and Standardize release_date
    - Extract day and month of "date_format
    - Combine year,day, month
    - Convert date_combined to yyyy-MM-dd format


<hr>
<a name='schemaref'></a>


https://www.kaggle.com/datasets/kapturovalexander/spotify-data-from-pyspark-course/data