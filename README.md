# 🚗 Gases Emitted by Vehicle — EDA & Machine Learning Project

A complete data science project that explores a vehicle emissions dataset through Exploratory Data Analysis (EDA) and builds multiple regression/classification models to predict the **Emission Level** of a vehicle based on its operating and environmental conditions.

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Model Building](#model-building)
- [Results](#results)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

---

## 📖 About the Project

Vehicle emissions are one of the largest contributors to air pollution and climate change. This project analyzes a synthetic dataset of vehicle operating conditions (engine size, speed, acceleration, mileage, road/traffic type, weather conditions, etc.) alongside their emitted gases (CO2, NOx, PM2.5, VOC, SO2) to:

1. Understand relationships between vehicle/environmental attributes and pollutant emissions.
2. Visualize emission patterns across vehicle types, fuel types, and driving conditions.
3. Build and compare multiple Machine Learning models that predict a vehicle's **Emission Level** (Low / Medium / High).

---

## 📊 Dataset

**File:** `vehicle_emission_dataset.csv`
**Records:** 10,000 rows
**Columns:** 19

| Column | Description |
|---|---|
| Vehicle Type | Car, Truck, Bus, Motorcycle |
| Fuel Type | Petrol, Diesel, Electric, Hybrid |
| Engine Size | Engine size in liters |
| Age of Vehicle | Age of the vehicle (years) |
| Mileage | Total distance traveled |
| Speed | Average vehicle speed |
| Acceleration | Average acceleration (m/s²) |
| Road Type | Highway, City, Rural |
| Traffic Conditions | Free flow, Moderate, Heavy |
| Temperature | Ambient temperature |
| Humidity | Ambient humidity |
| Wind Speed | Wind speed |
| Air Pressure | Atmospheric pressure |
| CO2 Emissions | Carbon dioxide emitted |
| NOx Emissions | Nitrogen oxide emitted |
| PM2.5 Emissions | Particulate matter emitted |
| VOC Emissions | Volatile organic compounds emitted |
| SO2 Emissions | Sulfur dioxide emitted |
| **Emission Level** | Target variable — Low / Medium / High |

The dataset has **no missing values** and **no duplicate rows**.

---

## 🔄 Project Workflow

```
Data Loading → Data Understanding → Data Cleaning →
Exploratory Data Analysis → Feature Encoding →
Train-Test Split → Model Training (multiple models & split ratios) →
Model Evaluation → Model Comparison → Conclusion
```

---

## 🛠 Tech Stack

- **Language:** Python 3
- **Data Handling:** NumPy, Pandas
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn (Linear Regression, Ridge, Lasso, ElasticNet)
- **Boosting Models:** XGBoost, LightGBM
- **Environment:** Jupyter Notebook

---

## 📁 Project Structure

```
vehicle-emission-analysis/
│
├── Gases_Emitted_by_Vehicle_EDA_and_LR.ipynb   # Main analysis & modeling notebook
├── vehicle_emission_dataset.csv                # Dataset used for the project
├── README.md                                   # Project documentation
└── requirements.txt                            # Python dependencies
```

---

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/vehicle-emission-analysis.git
   cd vehicle-emission-analysis
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

   Or install manually:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn xgboost lightgbm jupyter
   ```

---

## ▶️ Usage

1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Open `Gases_Emitted_by_Vehicle_EDA_and_LR.ipynb`.
3. Run all cells sequentially (`Kernel → Restart & Run All`) to reproduce the EDA, visualizations, and model results.

---

## 🔍 Exploratory Data Analysis

The notebook performs the following EDA steps:

- Dataset shape, structure, and data types (`.shape`, `.info()`, `.describe()`)
- Missing value check (`.isnull().sum()`) — none found
- Duplicate record check (`.duplicated().sum()`) — none found
- Distribution of the target variable `Emission Level` (histogram)
- Boxplots of weather-related features (Temperature, Humidity, Wind Speed)
- Boxplot of `CO2 Emissions` grouped by `Vehicle Type`
- Correlation matrix and heatmap of all numeric features

---

## 🤖 Model Building

Categorical columns are label-encoded, and the dataset is split into features (`X`) and target (`y = Emission Level`).

Six regression-based models were trained and compared across **three different train/test split ratios** (60/40, 80/20, 90/10):

| Model |
|---|
| Linear Regression |
| Ridge Regression |
| Lasso Regression |
| ElasticNet Regression |
| XGBoost Regressor |
| LightGBM Regressor |

Each model is evaluated using:

- **R² Score**
- **MAE** (Mean Absolute Error)
- **MSE** (Mean Squared Error)
- **RMSE** (Root Mean Squared Error)
- **MAPE** (Mean Absolute Percentage Error)

---

## 📈 Results

The results for every model/split combination are compiled into a single comparison table (see the final cells of the notebook) so the best-performing model and split ratio can be identified at a glance. Update this section with your final best-model summary once you've run the notebook end-to-end, e.g.:

> **Best Model:** `<model name>` at `<split>` split — R² Score: `<value>`%

---

## 🚀 Future Improvements

- Treat `Emission Level` as a classification problem and benchmark classifiers (Logistic Regression, Random Forest, XGBoost Classifier) alongside the current regression approach.
- Perform hyperparameter tuning (GridSearchCV / Optuna) on the top-performing models.
- Add feature importance / SHAP analysis to interpret model predictions.
- Deploy the best model as a simple web app (Streamlit/Flask).

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repository, open issues, or submit pull requests to improve the analysis or add new models.

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License — feel free to use and modify it for your own learning or research.

---

⭐ If you found this project useful, consider giving it a star on GitHub!
