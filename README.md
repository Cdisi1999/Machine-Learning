# Machine-Learning

# 🛢️ OilyGiant: Machine Learning for Oil Region Profitability

This project applies machine learning and statistical analysis to help **OilyGiant**, a mining company, choose the most profitable region for new oil well development. Using synthetic data from three surveyed regions, we build predictive models, calculate potential profits, and assess financial risks using the **bootstrapping** method.

## 📊 Objective

- Predict oil reserves in each region using **linear regression**
- Select the top 200 wells per region based on predicted reserves
- Estimate profits based on business constraints
- Evaluate risk using bootstrapping and recommend the best region

## 💼 Business Conditions

- 500 wells are sampled per region
- Only the top 200 wells will be developed
- Development budget: $100 million
- Revenue per 1,000 barrels: $4,500
- Only **Linear Regression** may be used
- Chosen region must have **< 2.5% chance of loss**

## 📁 Datasets

Three datasets are used:  
- `geo_data_0.csv`  
- `geo_data_1.csv`  
- `geo_data_2.csv`  

Each dataset contains:
- `id`: well identifier  
- `f0`, `f1`, `f2`: feature values  
- `product`: actual reserves (target, in 1,000 barrels)

## 🧪 Project Workflow

1. **Data Preparation**
   - Load and inspect data
   - Split into training and validation sets (75/25)

2. **Model Training & Evaluation**
   - Train linear regression models
   - Predict reserves and evaluate with RMSE

3. **Profit Estimation**
   - Calculate revenue from top 200 wells
   - Compute break-even reserve volume

4. **Risk Assessment**
   - Apply bootstrapping (1,000 samples)
   - Calculate:
     - Average profit
     - 95% confidence interval
     - Loss probability

5. **Conclusion**
   - Recommend the best region based on profit and risk

## 🧰 Tools Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- SciPy

## 📌 Key Result

After training models and analyzing the risk of loss in each region, we recommended the region that offered the **highest expected profit** while maintaining an **acceptable level of risk**.

---

📁 Project Notebook: `Machine Learning in Business.ipynb`
