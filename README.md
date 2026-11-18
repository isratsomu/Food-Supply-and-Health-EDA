 # 🌍 Global Food Supply, Obesity & COVID-19 Data Analysis

An Exploratory Data Analysis (EDA) project analyzing global food supply quantities (in kg/percentage), nutrition indicators (obesity and undernourishment), and COVID-19 statistics across 170 countries.

---

## 📌 Project Overview
This project explores the relationship between dietary patterns across different countries and continents, health metrics like obesity rates, and COVID-19 impact. By categorizing countries into their respective continents, the analysis uncovers regional trends in food consumption (such as animal fats, meat, and alcoholic beverages).

---

## 📂 Dataset Information
- **File Name:** `Food_Supply_Quantity_kg_Data.csv`
- **Initial Dimensions:** 170 rows (countries) × 32 columns
- **Cleaned Dimensions:** 154 rows × 33 columns (after removing missing values and adding a `region` column)
- **Key Features:**
  - **Food Categories:** Alcoholic Beverages, Animal Fats, Animal Products, Cereals, Eggs, Fish/Seafood, Fruits, Meat, Milk, Vegetables, Vegetal Products, etc. (measured as `%` of total food supply)
  - **Health & Nutrition:** `Obesity` (%), `Undernourished` (%).
  - **COVID-19 Metrics:** `Confirmed`, `Deaths`, `Recovered`, `Active` (% of population)
  - **Demographics:** `Country`, `Population`, and engineered `region` (Continent)

---

## 🛠️ Tech Stack & Libraries
- **Python 3**
- **Pandas** – Data loading, cleaning, grouping, and manipulation
- **NumPy** – Numerical operations
- **Matplotlib & Seaborn** – Data visualization setup
- **Google Colab** – Development environment

---

## 🔄 Workflow & Methodology
1. **Data Loading & Inspection:** Loaded the dataset in Google Colab and examined data types, summary statistics (`describe()`), and structure (`info()`)
2. **Data Cleaning:** 
   - Checked for duplicate records (0 duplicates found)
   - Identified and dropped rows containing missing (`NaN`) values across columns like `Obesity`, `Undernourished`, and COVID-19 metrics.
3. **Feature Engineering:** Mapped all countries into 6 major continents (`Africa`, `Europe`, `Asia`, `North America`, `South America`, `Oceania`) under a new `region` column.
4. **Statistical & Regional Analysis:** Performed correlation analysis, sorting, ranking (`nlargest` / `nsmallest`), and continent-wise `groupby` aggregations

---

## 📊 Key Findings & Insights

### 1. Obesity Statistics
- **Global Average Obesity Rate:** `18.45%`
- **Highest Obesity Rate:** `45.5%` (Samoa)
- **Top 5 Countries with Highest Obesity:**
  1. Samoa (`45.5%`)
  2. United States of America (`37.3%`)
  4. Saudi Arabia (`35.0%`)
  5. Jordan (`33.4%`)
- **Top 5 Countries with Lowest Obesity:** Vietnam (`2.1%`), Timor-Leste (`2.9%`), Bangladesh (`3.4%`), Cambodia (`3.5%`), Ethiopia (`3.6%`)

### 2. Regional Animal Fat Consumption (Mean %)
Europe leads significantly in animal fat consumption compared to other continents
| Region | Mean Animal Fats (%) |
| :--- | :---: |
| **Europe** | `0.5681`|
| **Oceania** | `0.2934`
| **Asia** | `0.1396`
| **North America** | `0.1342`
| **South America** | `0.1243` 
| **Africa** | `0.0627

### 3. Dietary Extremes
- **Highest Meat Consumption:** Mongolia (`8.0929%`)
- **Top Animal Product Consumers:** Finland (`26.89%`), Mongolia (`25.89%`), Netherlands (`24.30%`), Sweden (`24.06%`), Iceland (`23.97%`)
- **Highest Alcoholic Beverage Supply:** Burkina Faso (`15.37%`), Czechia (`9.85%`), Luxembourg (`8.09%`)
- **Lowest Alcoholic Beverage Supply:** Sudan, UAE, Saudi Arabia (`0.00%`)

### 4. Correlations
- **Animal Products & Obesity:** Moderate positive correlation (`0.52`), indicating higher animal-based food consumption aligns with higher obesity rates
- **Cereals & Obesity:** Negative correlation (`-0.55`), suggesting cereal-heavy diets correlate with lower obesity rates

---

## 🚀 How to Run the Project
1. Clone this repository:
   ```bash
   git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
