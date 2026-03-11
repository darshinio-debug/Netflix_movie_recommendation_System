# 🎬 Netflix Movie Recommendation System

## 📌 Project Overview

This project builds a **Movie Recommendation System** similar to Netflix using **Collaborative Filtering techniques**.
The system predicts how much a user will like a movie and recommends movies with the **highest predicted ratings**.

The goal of this project is to demonstrate **data preprocessing, exploratory data analysis, machine learning modeling, and recommendation generation** using Python.

---

## 📊 Dataset

The dataset contains movie ratings provided by users.

The original dataset is very large and cannot be uploaded to GitHub due to file size limits.
A small sample dataset is provided in the `dataset` folder for demonstration purposes.
To run the project with the full dataset, download it from:

https://www.kaggle.com/datasets/netflix-inc/netflix-prize-data

**Main Columns**

| Column   | Description                      |
| -------- | -------------------------------- |
| User_Id  | Unique identifier for each user  |
| Movie_Id | Unique identifier for each movie |
| Rating   | Rating given by the user         |

This dataset represents **user-movie interactions** which are used to train the recommendation model.

---

## ⚙️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Scikit-Surprise
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## 🧠 Recommendation Technique

This project uses **Collaborative Filtering** with the **SVD (Singular Value Decomposition)** algorithm.

### Steps Involved

1. Data Preprocessing
2. Exploratory Data Analysis (EDA)
3. Preparing the Dataset for the Model
4. Training the Recommendation Model
5. Predicting Ratings for Unseen Movies
6. Recommending Top Movies for the User

---

## 📈 Model Evaluation

The recommendation model is evaluated using **Root Mean Square Error (RMSE)**.

Example cross-validation:

```
from surprise.model_selection import cross_validate

cross_validate(model, data, measures=['RMSE'], cv=3, verbose=True)
```

Lower RMSE indicates **better prediction accuracy**.

---

## 🎥 Recommendation Process

The recommendation system follows these steps:

1. Identify movies already watched by the user
2. Remove watched movies from the recommendation list
3. Predict ratings for unseen movies
4. Rank movies based on predicted ratings
5. Recommend the **top movies with highest predicted scores**

Example prediction:

```
model.predict(user_id, movie_id)
```

The predicted rating is extracted using:

```
.est
```

---

## 📷 Example Recommendation Output

Example of top recommended movies for a user:

| Movie           | Predicted Rating |
| --------------- | ---------------- |
| Interstellar    | 4.85             |
| Inception       | 4.79             |
| The Matrix      | 4.73             |
| The Dark Knight | 4.70             |
| Avengers        | 4.68             |

---

## 📁 Project Structure

```
Netflix-Recommendation-System
│
├── Netflix_Recommendation_system.ipynb
├── dataset
│   ├── ratings.csv
│   └── movies.csv
│
├── images
│   ├── recommendation_output.png
│
├── requirements.txt
└── README.md
```

---

## 🚀 How to Run the Project

### 1️⃣ Clone the repository

```
git clone https://github.com/yourusername/Netflix-Recommendation-System.git
```

### 2️⃣ Install dependencies

```
pip install -r requirements.txt
```

### 3️⃣ Run the notebook

Open and run:

```
Netflix Recommendation system.ipynb
```

---

## 💡 Future Improvements

* Hybrid Recommendation System
* Deep Learning based Recommender Systems
* Real-Time Recommendation API
* Web Application using Streamlit or Flask

---

## 👩‍💻 Author

**Darshini**

AI & Data Analytics Enthusiast
Interested in **Machine Learning, Recommendation Systems, and AI Applications**

-----
MIT LICENSE

