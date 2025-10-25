# crop-recommendation-using-weather-and-soil-content

# 🌾 Crop Recommendation System

A **Machine Learning-based web application** that recommends the most suitable crop to grow based on soil and weather parameters such as Nitrogen (N), Phosphorus (P), Potassium (K), temperature, humidity, pH, and rainfall.

This project was built **from scratch** using Python (Jupyter Notebook) and Flask for the backend, with a simple HTML, CSS, and JS-based frontend.



## 📘 Project Overview

This system uses **machine learning algorithms** to predict the best crop suited for given environmental and soil conditions.
The dataset contains over **2000+ entries** of different crops including rice, maize, chickpea, kidney beans, pigeon peas, moth beans, mung beans, black gram, lentil, pomegranate, banana, mango, grapes, watermelon, muskmelon, apple, orange, papaya, coconut, cotton, jute, and coffee.



## 🧪 Machine Learning Model

### 🔹 Libraries Used

* **Pandas** – for data manipulation and analysis
* **NumPy** – for numerical operations
* **Scikit-learn** – for machine learning model training and evaluation
* **Matplotlib** – for data visualization

### 🔹 Dataset

**File:** `Crop_recommendation.csv`
**Attributes:**

| Feature            | Description                                                      |
| ------------------ | ---------------------------------------------------------------- |
| **N (Nitrogen)**   | Essential for leaf growth and chlorophyll production             |
| **P (Phosphorus)** | Helps in root development and energy transfer                    |
| **K (Potassium)**  | Improves plant strength and resistance to diseases               |
| **Temperature**    | Affects crop growth rate and development                         |
| **Humidity**       | Influences transpiration and water absorption                    |
| **pH**             | Determines soil acidity or alkalinity, affecting nutrient uptake |
| **Rainfall**       | Provides necessary water supply for crop growth                  |



## ⚙️ Model Training and Evaluation

The model was trained and tested using a **train-test split** approach on four algorithms:

| Algorithm           | Accuracy |
| ------------------- | -------- |
| Logistic Regression | 97.27%   |
| Decision Tree       | 97.81%   |
| Naive Bayes         | 99.45%   |
| Random Forest       | 99.45%   |

Among these, **Random Forest** achieved the highest accuracy and handled overfitting better than others.
Hence, it was selected as the final model.



## 💾 Model Saving Using Joblib

The trained model was saved using the **Joblib** library.

**About Joblib:**
Joblib is a lightweight Python library used for **serializing and deserializing Python objects** efficiently. It is particularly useful for saving large NumPy arrays or machine learning models.

* It stores the model in a compressed binary format.
* Faster than `pickle` for large data.
* Enables quick reloading of models without retraining.
* Helps maintain reproducibility of results.
* Makes deployment easier in web applications.

The final model was saved as **`crop_app`**.



## 🧩 Flask Application (Backend)

### **File:** `crop_app.py`

A Flask web application is developed to interact with the trained ML model.

**Workflow Summary:**

* Imports necessary libraries (`Flask`, `joblib`).
* Loads the pre-trained model (`crop_app`).
* Renders the home page (`Home_1.html`) and prediction page (`Index.html`).
* Accepts user inputs for N, P, K, temperature, humidity, pH, and rainfall via a form.
* Validates inputs and predicts the most suitable crop using the loaded model.
* Displays the result on the prediction page.



## 🎨 Frontend Overview

* **Templates Folder:** Contains HTML files (`Home_1.html`, `Index.html`, `prediction.html`) for different routes.
* **Static Folder:** Contains CSS files and background images for styling and design.

Frontend is designed with **basic HTML, CSS, and JavaScript**, ensuring simplicity and clarity for users.



## 📊 Additional Work

Before starting the project, a **survey** was conducted to gather insights from users and farmers.
The survey received **51 responses**, covering aspects such as:

* Age group of respondents
* Familiarity with agricultural purposes
* Soil characteristics considered while selecting crops
* Interest in digital tools for crop recommendation
* Expected features in such a tool

The complete responses are available in **`survey_responses.pdf`** in this repository.

Additionally:

* A **Telugu explanation video (.mp4)** made using **NotebookLM** is included.
* The repository also contains **project documentation** and a **presentation (PPT)** for reference.



## 🚀 How to Run the Project

### **Step 1:** Download the Repository

Click on the **“Code” → “Download ZIP”** option and extract it.

### **Step 2:** Run the Machine Learning Notebook

1. Open `crop_prediction.ipynb` in **Jupyter Notebook**.
2. Run all the cells to train and test the models.
3. Ensure there are no errors related to library versions.
4. The newly generated **`crop_app`** model file should replace the existing one in the repository.

### **Step 3:** Configure Flask App

* Open the project folder in **VS Code**.
* Update the model path in `crop_app.py` if necessary.

### **Step 4:** Run the Flask Application

* Keep only `crop_app.py` open and click **Run** at the top.
* The terminal will display a local server link like `https://localhost:5000`.
* Open the link in your browser.

### **Step 5:** Use the Web App

1. Click on **Predict** on the home page.
2. Enter values for N, P, K, temperature, humidity, pH, and rainfall.
3. Click **Predict** again.
4. The result page will display the **recommended crop** for the given conditions.



## 🤝 Contributions

Contributions, ideas, or further developments (like deployment, UI improvement, or adding new models) are **welcome**!
You can **fork this repository** and experiment with your own enhancements.



## 📂 Repository Contents

```
Crop_Recommendation_System/
│
├── crop_prediction.ipynb       # Jupyter Notebook for ML model
├── crop_app.py                 # Flask backend code
├── Crop_recommendation.csv     # Dataset
├── survey_responses.pdf        # Survey data
├── explanation_telugu.mp4      # Project explanation in Telugu
├── documentation.pdf           # Detailed project documentation
├── presentation.pptx           # Project presentation
├── static/                     # CSS and images
├── templates/                  # HTML files
└── crop_app                    # Saved ML model
```

## Output images -
first page-
<img width="1919" height="906" alt="image" src="https://github.com/user-attachments/assets/f8befcdf-d260-4668-ab44-71e3a3d95aec" />
second page-
<img width="1892" height="909" alt="image" src="https://github.com/user-attachments/assets/6043ea1a-8595-47ff-97f9-9b1c59aae7cb" />
third page-
<img width="1897" height="905" alt="image" src="https://github.com/user-attachments/assets/895e268d-d58a-4181-8a8b-600c08e24ce5" />


## 🧑‍💻 Author

**N. Pooja**
B.Tech (CSE - Data Science)
GitHub: [@pooja742](https://github.com/pooja742)
