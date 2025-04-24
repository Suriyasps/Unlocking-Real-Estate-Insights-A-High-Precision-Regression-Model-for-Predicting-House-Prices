# Unlocking Real Estate Insights: A High-Precision Regression Model for Predicting House Prices

## 📌 Introduction

In today's competitive real estate market, machine learning is crucial for accurately predicting house prices. This project explores a regression model using the Ames housing dataset, emphasizing statistical rigor and model precision.

### Key Objectives:
- Explore significant predictors of house prices
- Implement regression modeling in R
- Visualize relationships between variables and sale prices
- Test model assumptions and performance

---

## 📊 Hypotheses

1. **House Quality**: Higher quality = Higher sale price  
2. **Constructed Area**: Larger built-up area = Higher price  
3. **Year Built**: Newer homes = Higher value  
4. **Bathrooms**: More full bathrooms = Higher sale price  
5. **Year Remodeled**: Recent remodel = Increased value  
6. **Number of Rooms**: More rooms = Higher market value  

---

## 🧪 Methodology

- **Dataset**: Ames housing data with ~79 variables and 2,880 observations
- **Tool**: R (with `ggplot2`, `tidyverse`, `caret`, etc.)
- **Steps**:
  - Data cleaning & transformation
  - Exploratory data analysis & visualization
  - Regression modeling (5 iterative models)
  - Validation via residual, Q-Q plots, VIF, Durbin-Watson test

---

## 📈 Key Visualizations

- **Quality vs. Price**: Spearman's ρ = 0.81
- **Floor Area vs. Price**: Parabolic trend, Pearson's r ≈ 0.58
- **Year Built vs. Price**: Positive trend, ρ ≈ 0.68
- **Bathrooms vs. Price**: Increases until 3 bathrooms
- **Remodel Year vs. Price**: Positive trend, ρ ≈ 0.60
- **Total Rooms vs. Price**: Moderate positive correlation, ρ ≈ 0.49

---

## 🧮 Regression Models

Built using stepwise addition of variables to improve predictive performance:

| Model | Adjusted R² | Key Additions |
|-------|--------------|----------------|
| 1     | 0.781        | Core variables (quality, floor area, etc.) |
| 2     | 0.798        | Added lot area, house condition |
| 3     | 0.81+        | Added roof type, stories |
| 4     | 0.83+        | Added garage area, kitchen quality |
| 5     | 0.855        | Final model, added veneer area |

- **Final RMSE**: \$35,435  
- **MAE**: \$20,049  
- **Test R²**: 0.83

---

## ✔️ Assumption Checks

- **Residual Plot**: Some heteroscedasticity; mostly well-distributed
- **Q-Q Plot**: Data mostly follows normal distribution
- **Durbin-Watson**: 2.02 (no autocorrelation)
- **VIF**: All < 5 (no serious multicollinearity)
- **Cook’s Distance**: No overly influential points

---

## ✅ Conclusion

The regression model shows strong predictive performance and robustness, offering a reliable tool for house price estimation. It highlights machine learning’s value in enhancing real estate decision-making. While some variance remains unexplained (likely due to missing data), the model demonstrates excellent accuracy for practical use.

---
