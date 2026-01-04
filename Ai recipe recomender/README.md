# 🍽️ Recipe Recommendation System (AI-Based)

## Project Overview

Recipe Recommendation System is an AI-powered web application that recommends suitable recipes based on user-provided nutritional values and ingredients.  
It uses machine learning similarity matching to identify recipes that closely align with the user’s dietary requirements.

The system combines numerical nutrition data with text-based ingredient analysis, making the recommendations more accurate and meaningful.

## Objectives

- Recommend recipes based on nutritional constraints such as calories, fat, protein, and carbohydrates.
- Integrate numerical and textual data for intelligent similarity matching.
- Provide a simple and interactive web-based interface.
- Demonstrate a real-world application of machine learning in food and nutrition systems.

## System Working (AI Logic)

1. User enters nutritional values and ingredient preferences.
2. Numerical features are normalized using StandardScaler.
3. Ingredients are converted into vectors using TF-IDF Vectorization.
4. Numerical and textual features are combined into a single feature space.
5. K-Nearest Neighbors (KNN) identifies the most similar recipes.
6. Top matching recipes are displayed to the user.

## System Architecture

┌─────────────────┐
│ User Input │
│ (Nutrition + │
│ Ingredients) │
└────────┬────────┘
│
▼
┌─────────────────┐
│ Data Validation │
│ & Preprocessing │
└────────┬────────┘
│
▼
┌─────────────────────────────────┐
│ Feature Engineering │
│ ┌──────────────┬──────────────┐│
│ │ StandardScaler│ TF-IDF ││
│ │ (Nutrition) │ (Ingredients)││
│ └──────┬────────┴──────┬──────┘│
└─────────┼───────────────┼───────┘
│ │
└───────┬───────┘
│
▼
┌────────────────┐
│ Feature Fusion │
│ (Concatenation)│
└────────┬───────┘
│
▼
┌────────────────┐
│ KNN Algorithm │
│ (k=5 neighbors)│
└────────┬───────┘
│
▼
┌────────────────┐
│ Top Recipes │
│ (Ranked Results)│
└────────────────┘

## Machine Learning Techniques Used

- K-Nearest Neighbors (KNN) – similarity-based recommendation.
- TF-IDF Vectorizer – ingredient text processing.
- StandardScaler – normalization of nutritional features.

## Technologies Used

### Frontend

- HTML5
- CSS3
- Bootstrap 4

### Backend

- Python
- Flask

### Machine Learning & Data Processing

- Scikit-learn
- NumPy
- Pandas

## Dataset Description

The dataset includes:

- Recipe names
- Nutritional attributes (calories, fat, carbohydrates, protein, cholesterol, sodium, fiber)
- Ingredient lists
- Recipe image URLs

All data is preprocessed before training to ensure consistency and reliable recommendations.

## Key Features

- Nutrition-based recipe recommendations.
- Ingredient-aware similarity matching.
- Clean and responsive user interface.
- Fast predictions using KNN.
- Visual recipe cards with images.

## How to Run the Project

### 1) Clone the Repository

```bash
git clone <your-repository-link>
cd recipe-recommendation-system

```

### 2) Install Dependencies

pip install flask numpy pandas scikit-learn

### 3) Run the Application

python app.py

### 4) Open in Browser

http://127.0.0.1:5000/

python app.py

```

### 5️⃣ Access the Application

Open your browser and navigate to:
```

http://127.0.0.1:5000/

```

---

## Project Structure
```

recipe-recommendation-system/
│
├── app.py # Flask application and API routes
├── model.py # ML model training and prediction logic
├── requirements.txt # Python dependencies
├── dataset/
│ └── recipes.csv # Recipe dataset
├── static/
│ ├── css/
│ │ └── style.css # Custom styles
│ └── images/ # Static images
├── templates/
│ ├── index.html # Homepage
│ └── results.html # Results page
└── README.md # Project documentation
