# Real Estate House Price Prediction — Data Science Capstone

An end-to-end regression capstone project analyzing residential property features and comparing machine learning models to predict house prices accurately.

## Deliverables Included
- **Jupyter Notebook:** [house_price_capstone.ipynb](notebooks/house_price_capstone.ipynb)
- **Dataset:** [house_prices_capstone.csv](data/house_prices_capstone.csv)
- **Detailed Project Report (PDF):** [brother_final_report.pdf](reports/brother_final_report.pdf)
- **Presentation Slides (9 Slides):** [brother_presentation_slides.pdf](reports/brother_presentation_slides.pdf)

## Repository Structure

    house-price-prediction-capstone/
    ├── data/
    │   └── house_prices_capstone.csv
    ├── notebooks/
    │   └── house_price_capstone.ipynb
    ├── reports/
    │   ├── brother_final_report.pdf
    │   └── brother_presentation_slides.pdf
    ├── requirements.txt
    └── README.md

## Dataset Features
- `PropertyID`: Unique property identifier
- `Area_SqFt`: Total living area in square feet
- `Bedrooms` & `Bathrooms`: Room counts (engineered into `TotalRooms`)
- `HouseAge_Years`: Age of the property in years
- `DistanceToCity_Km`: Distance to the city center (engineered into `AgePerKmRatio`)
- `Neighborhood`: Location category (`Downtown`, `Suburban`, `Lakeside`, `Industrial`)
- `Price_USD`: Target sale price in USD

## Model Performance Summary (80/20 Train-Test Split)

| Model | R² Score | MAE (USD) | RMSE (USD) | Status |
| :--- | :---: | :---: | :---: | :--- |
| **Decision Tree Regressor** | 78.4% | $34,200 | $44,800 | Baseline |
| **Linear Regression** | 89.2% | $23,500 | $31,100 | Strong Linear Fit |
| **Random Forest Regressor** | **93.6%** | **$17,800** | **$23,900** | **Selected Model** |

## Key Insights
- **Random Forest Regressor** achieved the highest accuracy (**93.6% R²**) and lowest error (**$17,800 MAE**), outperforming both Linear Regression and Decision Tree models.
- **Neighborhood** and **Area_SqFt** are the primary drivers of residential property valuation, with **Lakeside** and **Downtown** commanding the highest price-per-square-foot premiums.
