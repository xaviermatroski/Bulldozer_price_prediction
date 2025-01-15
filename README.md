# Blue Book for Bulldozers

Welcome to the **Blue Book for Bulldozers** project! This repository demonstrates a solution to predicting auction prices for heavy equipment, using data from [Kaggle](https://www.kaggle.com/c/bluebook-for-bulldozers). The project incorporates data preprocessing, feature engineering, and advanced machine learning techniques to build a robust predictive model.

## Dataset Overview 📊
The dataset provides information about sales of bulldozers over time, including features such as:
- **Sales ID**: Unique identifier of the sale.
- **SalePrice**: Target variable representing the sale price of the bulldozer.
- **MachineID**: Unique identifier for the machine.
- **UsageBand**: Categorization of usage (e.g., low, medium, high).
- **ModelID**: Identifier for the specific machine model.
- **saledate**: Date of the sale.

## Key Features of This Project 🚀

1. **Data Exploration:**
   - Analyzed missing values, data types, and distributions of key features.
   - Visualized sale prices over time to understand trends and seasonality.

2. **Feature Engineering:**
   - Extracted datetime components (year, month, day, day of the week, day of the year) from the `saledate` feature.
   - Handled missing values in numerical features by imputing medians and added indicator columns for missingness.
   - Converted categorical features to numeric codes for model compatibility.

3. **Model Building:**
   - Utilized **Random Forest Regressor** as the primary machine learning model.
   - Split the dataset into training (data before 2012) and validation (data from 2012) sets.

4. **Model Evaluation:**
   - Designed custom evaluation functions such as **Root Mean Squared Log Error (RMSLE)**.
   - Compared metrics like MAE, RMSLE, and R² to assess model performance.

5. **Hyperparameter Tuning:**
   - Performed Randomized Search to optimize hyperparameters such as the number of estimators, maximum depth, and minimum samples per leaf.

## Results 🎯
The ideal model achieved the following metrics:

- **Training MAE**: 2953.82
- **Validation MAE**: 5951.25
- **Training RMSLE**: 0.1447
- **Validation RMSLE**: 0.2452
- **Training R²**: 0.9588
- **Validation R²**: 0.8818

## How to Run the Project 🖥️

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/blue-book-for-bulldozers.git
   cd blue-book-for-bulldozers
   ```
2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the dataset from [Kaggle](https://www.kaggle.com/c/bluebook-for-bulldozers/data) and place it in the `data/` directory.
4. Run the main script:
   ```bash
   python main.py
   ```

## Next Steps 📈
- Experiment with additional models such as Gradient Boosting or XGBoost.
- Deploy the model using Flask or Streamlit for interactive predictions.
- Conduct feature importance analysis to identify key drivers of sale price.

## Contributions 🌟
Feel free to fork this repository and create a pull request for any improvements or new ideas. Feedback and suggestions are always welcome!

## Acknowledgments 🙌
- Dataset provided by [Kaggle](https://www.kaggle.com/c/bluebook-for-bulldozers).
- Special thanks to the data science community for valuable resources and support.

---

**Let’s predict with precision!**

