# **🌾 Developing Predictive Models for Pest Incidence with Integration of Satellite Images and Weather Data for Location-Specific Predictions** 🌍

### **📚 Project Overview**
This project was developed in collaboration with the [**WOTR (Watershed Organization Trust)**](https://wotr.org/) as part of our academic requirements. The goal was to build predictive models for **pest incidence** in crops, integrating **satellite images** 🌌 and **weather data** ☀️🌧️ to make **location-specific predictions**. The datasets provided included **crop-specific pest incidence data** and **weather data** from districts in Maharashtra, India 🌏. The objective was to predict the presence or absence of pests for different crops based on available data.

### **🌍 About [WOTR (Watershed Organization Trust)](https://wotr.org/)**
Founded in **1993**, WOTR is a non-profit organization focused on **water and food security**, **livelihoods**, and **sustainable growth** in rural India. Over the past three decades, WOTR has worked in **7124 villages** across **10 states**, impacting over **6.93 million people**. The organization has regenerated over **2.64 million hectares** of degraded landscapes, created **158 billion liters** of water harvesting capacity, and significantly boosted agricultural productivity.
**Key Focus Areas:**
- 🌿 **Agriculture**
- 👩‍🌾 **Women Empowerment**
- 💧 **Water & Land Management**
- 🌾 **Livelihoods**
- 🩺 **Health, Sanitation & Nutrition**

### **📊 Datasets**
We were provided with two key datasets:
1. **Pest Incidence Data**: Contained pest occurrence records over time for different crops, with ~150k data points. The data included different crop types 🌾 and their respective pest incidences 🐛 across various locations in Maharashtra.
2. **Weather Data**: A 5-year weather dataset 🌦️ for the same districts, detailing parameters such as temperature 🌡️, humidity 💧, precipitation 🌧️, and other meteorological factors.

### **🔧 Data Preprocessing**
The initial dataset contained approximately **150k data points**, which was reduced to **70k data points** after data cleaning for binary classification (pest occurrence vs. no pest). Steps included:
- **Cleaning the Pest Incidence Data**: Cleaned and filtered rows to focus on crops with sufficient data points (>1000) 🍃.
- **Weather Data**: Cleaned and integrated with pest data, ensuring alignment with pest observation dates 🗓️.
- **Satellite Data Integration**: We used **Google Earth Engine (GEE)** to pull **Sentinel satellite imagery** 🛰️, from which we extracted **vegetative indices** for the inspection dates. We also integrated **geographical coordinates (latitudes and longitudes)** 🌍 for accurate location-based predictions.

### **📈 Exploratory Data Analysis (EDA)**
We performed extensive **EDA** on both the cleaned pest dataset and weather data:
- **Crop-Specific Trends**: We analyzed pest incidences over time for different crops 🌱.
- **Weather Impact**: We examined how weather variables (temperature, humidity, etc.) influenced pest occurrences 🌡️.
- **Integration of Satellite Indices**: We explored how vegetation indices derived from satellite images correlated with pest occurrences 🌿.

### **🤖 Models and Approach**
We experimented with **five different machine learning models** to predict pest incidences:
1. **Logistic Regression** 📊
2. **Random Forest** 🌳
3. **XGBoost** 🚀
4. **Support Vector Machine (SVM)** 💻
5. **Explainable Boosting Machine (EBM)** 🔍

We explored **three different training approaches**:
- **All crops with all pests**: A global model for all crops and pests combined 🌾🐛.
- **Per crop with all pests**: A model for each crop, predicting all pests 🌿🐜.
- **Per crop, per pest**: A model for each crop and each pest individually 🌽🐞.

### **🏆 Results and Insights**
- **Best Performing Models**: Both **XGBoost** and **Random Forest** consistently performed the best across different training approaches. However, we observed that the performance of models varied depending on the training scenario. For some crops or pests, certain models performed better than others.
- **Impact of Satellite Data**: Integrating vegetation indices from satellite imagery improved model performance by **3%**. This demonstrates the valuable contribution of satellite data to predicting pest occurrences 🌾📸🌍.

### **📜 Conclusion and Recommendations**
We delivered our results to WOTR, along with **recommendations** for improving pest prediction capabilities:
- **Data Collection**: We advised on improving the granularity of pest data collection, especially increasing the frequency of inspections 🧐.
- **Inspection Procedures**: Better field inspection and geo-location data 📍 can enhance model accuracy, especially when integrated with weather and satellite data.

### **📦 Project Deliverables**
- Cleaned and processed datasets with pest incidence and weather data 🧹.
- Developed and tested predictive models for pest prediction 🔮.
- Results and analysis of model performance and impact of satellite data 📊.
- Final report and recommendations for WOTR on improving pest prediction methods 📝.

### **💻 Technologies Used**
- **Python** 🐍 (for data cleaning, analysis, and model training)
- **Google Earth Engine** 🌐 (for satellite image processing)
- **Scikit-learn**, **XGBoost**, **EBM**, **SVM** 🔧 (for model development)
- **Pandas**, **NumPy**, **Matplotlib**, **Seaborn** 📊 (for data manipulation and visualization)
- **Jupyter Notebooks** 📚 (for experimentation and documentation)


🙏🏻 _We would like to extend our sincere gratitude to **WOTR** for providing us with the opportunity to work with them on this project. Their invaluable support allowed us to apply our knowledge and skills in real-world scenarios, contributing to the critical work of improving agricultural practices and livelihood security for vulnerable communities in rural India. 🌾
We appreciate the **collaboration** and the opportunity to contribute to WOTR's ongoing mission to support sustainable development and empower rural communities. Thank you, WOTR! 💚_
