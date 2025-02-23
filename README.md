# 🙏 **Tribute to Surendar Manoj Sir** 🙏

This project is dedicated to **Surendar Manoj Sir**, whose YouTube channel has been an invaluable resource for learning data analysis and programming. His tutorials and guidance have inspired countless learners, including myself, to explore the world of data science and programming. Thank you, Sir, for your dedication and generosity in sharing knowledge! 🌟

---

# 🍽️ Zomato Restaurant Data Analysis 📊

This repository contains a Jupyter Notebook (`Untitled9.ipynb`) that processes and analyzes restaurant data from Zomato. The data was sourced from **Surendar Manoj Sir's Google Drive**, and the notebook demonstrates how to load, clean, and explore the data using Python and pandas.

## **Table of Contents** 📑
1. [Project Overview](#project-overview-)
2. [Key Features](#key-features-)
3. [Code Explanation](#code-explanation-)
4. [How to Use](#how-to-use-)
5. [Future Improvements](#future-improvements-)
6. [Contributing](#contributing-)

---

## **Project Overview** 🚀

This project focuses on processing JSON data from Zomato, which contains information about restaurants such as:
- Restaurant names 🏠
- Cuisines 🍕
- Ratings ⭐
- Locations 📍
- Online delivery availability 🚚
- And more!

The goal is to convert this JSON data into a structured format (pandas DataFrame) and perform basic data exploration and analysis.

---

## **Key Features** ✨

- **JSON Data Loading**: Loads restaurant data from JSON files.
- **Data Cleaning**: Handles missing values and extracts relevant information.
- **Data Exploration**: Provides insights into the dataset, such as the number of restaurants, cuisines, and ratings.
- **Pandas Integration**: Uses pandas to manipulate and analyze the data efficiently.

---

## **Code Explanation** 🧑‍💻

### **1. Importing Libraries** 📚
The notebook starts by importing the necessary libraries:
- `pandas` for data manipulation.
- `json` for handling JSON data.

```python
import pandas as pd
import json



#2. Loading JSON Data 📂
file_path = r"C:\\Users\\avina\\Downloads\\json\\file1.json"
with open(file_path, "r", encoding="utf-8") as f:
    data = json.load(f)

#3.Extracting Restaurant Data 🍴
all_restaurants = []
for page in data:
    if "restaurants" in page:
        all_restaurants.extend([restaurant["restaurant"] for restaurant in page["restaurants"]])

4. Creating a DataFrame 📊
df = pd.json_normalize(all_restaurants)

5. Exploring the Data 🔍
print(df.shape)  # Number of rows and columns
print(df.head())  # First 5 rows
print(df.isna().sum())  # Missing values

How to Use 🛠️
Clone the Repository:
git clone https://github.com/ABILASHGOVINDH/JSON-to-Data-Frame-Conversion.git

pip install pandas

Contributing 🤝
Contributions are welcome! If you'd like to improve this project, feel free to:

Fork the repository.
Create a new branch for your changes.
Submit a pull request.

