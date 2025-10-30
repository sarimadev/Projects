# Decoding Urban Emissions: Predictive Modeling and Data Analysis

**MSc Data Science Dissertation | Middlesex University | January 2024**

---

## 📊 Overview

This research investigates how different vehicular fuel types impact urban air quality under varying meteorological conditions in the London Borough of Barnet. Using advanced machine learning techniques including Multivariate LSTM networks, Random Forest, and Support Vector Regression, the study analyzed 116 months of traffic, air quality, and weather data to provide actionable insights for policymakers and urban planners.

**Key Finding:** Diesel vehicles, particularly Heavy Goods Vehicles (HGVs), are the primary contributors to NO₂ and particulate matter (PM2.5, PM10) pollution in urban areas, with meteorological conditions like wind speed and temperature significantly moderating pollutant dispersion.

---

## 🎯 Research Objectives

1. Analyze correlations between vehicular fuel types and key urban air pollutants (NO₂, CO, SO₂, PM10, PM2.5)
2. Examine how meteorological conditions influence emission impacts on air quality
3. Develop predictive models to forecast pollution levels using machine learning

---

## 🔬 Methodology

### Study Area
**London Borough of Barnet** — High-traffic urban area with major routes including the North Circular and M1 motorway.

### Data Sources
- **Traffic Data:** Department for Transport (hourly vehicle counts by type)
- **Air Quality:** DEFRA AURN & OpenWeather API (NO₂, PM10, PM2.5, SO₂, CO)
- **Weather Data:** OpenWeather API (temperature, wind, humidity, precipitation)
- **Vehicle Statistics:** DVLA licensing data (fuel type distributions)
- **Emission Factors:** National Atmospheric Emissions Inventory (NAEI)

**Period:** 2021-2022 | **Final Dataset:** 15,619 observations across 19 engineered features

### Machine Learning Models
- **Random Forest Regressor** — Handles multicollinearity and large feature spaces
- **Support Vector Regressor (SVR)** — Captures non-linear relationships
- **Multivariate LSTM Networks** — Models temporal dependencies in time-series data

---

## 📈 Key Findings

### Emission-Pollutant Relationships
✅ **Diesel HGVs** show strong positive correlation with NO₂ and particulate matter  
✅ **Petrol cars** contribute to PM10 but less significantly than diesel  
✅ **Granger causality** established between diesel HGV emissions and SO₂ levels

### Meteorological Impact
🌬️ **Wind speed** — Consistent negative correlation with all pollutants (dispersion effect)  
🌡️ **Temperature** — Complex relationship; increases PM2.5 through atmospheric reactions  
💧 **Humidity** — Positively correlates with NO₂  

### Model Performance
| Pollutant | Best Model | R² | Key Insight |
|-----------|------------|-----|-------------|
| **NO₂** | SVR | 0.405 | Captures 40.5% of variance |
| **CO** | LSTM | 0.198 | Low error rates, promising results |
| **PM2.5** | LSTM | 0.191 | Best among particulate predictions |
| **SO₂** | SVR | 0.230 | Complex emission dynamics |
| **PM10** | All | <0.1 | Requires further refinement |

**Key Takeaway:** LSTM networks excel at predicting pollutants with strong temporal patterns (CO, NO₂), while particulate matter remains challenging across all model types.

---

## 💡 Impact & Applications

**For Policymakers:**
- Evidence-based targeting of diesel HGV regulations
- Data-driven emission reduction strategies during adverse weather

**For Urban Planners:**
- Traffic management insights to minimize pollution exposure
- Infrastructure planning for air quality improvement

**For Environmental Agencies:**
- Predictive tools for air quality monitoring
- Early warning systems for high-pollution events

---

## 🛠️ Tools & Technologies

**Programming:** Python (Pandas, NumPy, Scikit-learn, TensorFlow/Keras)  
**Data Collection:** RESTful APIs, Government databases  
**Statistical Analysis:** Spearman correlation, Granger causality, Multiple regression  
**Visualization:** Matplotlib, Seaborn  
**Environment:** Google Colab (Jupyter Notebook)

---

## 📂 Repository Contents

- **`Dissertation/`** — Full research dissertation (58 pages) including methodology, analysis, and results
- **`README.md`** — Project overview and key findings
- **`LICENSE`** — Terms of use

**Note:** Code and datasets are not included in this repository. Full implementation details are available in the dissertation. For collaboration or access to materials, please contact me directly.

---

## ⚠️ Study Limitations

- Traffic data gaps required interpolation
- 2022 emission factors estimated via extrapolation
- Hybrid vehicles excluded due to insufficient data
- Particulate matter predictions require improvement

---

## 🎓 Academic Context

**Institution:** Middlesex University, London  
**Programme:** MSc Data Science  
**Supervisor:** Prof. Serengul Smith  
**Completion:** January 2024

---

## 📜 License

This project is shared for educational and portfolio purposes.  
© 2024 Sarima Iyayi. All rights reserved.

**Data Sources:**
- ONS UK HPI: [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/)
- DEFRA Air Quality: Crown copyright
- OpenWeather: Commercial API license

---

## 👤 Author

**Sarima Iyayi**  
MSc Data Science | Environmental Data Analyst | Machine Learning Practitioner

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?logo=linkedin)](YOUR_LINKEDIN_PROFILE)  
[![Email](https://img.shields.io/badge/Email-Contact-D14836?logo=gmail)](mailto:YOUR_EMAIL)  
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-4CAF50)](YOUR_PORTFOLIO_LINK)

---

### 💬 Interested in collaboration or have questions about this research?  
**Feel free to reach out — I'm always happy to discuss urban emissions, predictive modeling, or data science applications in environmental research!**

---

*For access to code implementation, detailed model architectures, or research collaboration, please contact me directly.*

---

*Last updated: October 2025*
