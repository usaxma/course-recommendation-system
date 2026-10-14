# Course Recommendation System

Content-based course recommender on Udemy catalog data. Titles are cleaned, vectorized, and ranked with cosine similarity. A Flask app plus an analytics dashboard sit on top of the same dataset.

## Skills

- Text cleaning (`neattext`)
- CountVectorizer / TF-IDF
- Cosine similarity and linear kernel
- Exploratory analysis of price, subscribers, and subject mix
- Flask search + recommendation API-style routes
- Plotly/HTML dashboard of catalog KPIs

## Dataset

`notebooks/udemy_course_data.csv` — course title, URL, price, subscribers, level, duration.  
`app/UdemyCleanedTitle.csv` — same table with a cleaned title column used at inference.

## Run the notebooks

```bash
pip install -r requirements.txt
jupyter notebook notebooks/EDA_Udemy_Dataset.ipynb
jupyter notebook notebooks/Course_Recommendation_System.ipynb
```

## Run the app

```bash
cd app
pip install -r ../requirements.txt
python app.py
```

- `/` — type a course title (or a keyword) to get similar courses  
- `/dashboard` — catalog charts (levels, subjects, yearly profit proxy)

## Structure

```
course-recommendation-system/
├── notebooks/
│   ├── Course_Recommendation_System.ipynb
│   ├── EDA_Udemy_Dataset.ipynb
│   └── udemy_course_data.csv
├── app/
│   ├── app.py
│   ├── dashboard.py
│   ├── UdemyCleanedTitle.csv
│   └── templates/
├── requirements.txt
└── README.md
```
