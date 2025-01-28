
# Credit Scoring and Risk Prediction for Loan Optimization at Bati Bank Using Machine Learning Techniques 📊💳

## Project Overview 🌍

This project aims to create a credit scoring model for **Bati Bank**, a leading financial service provider, in collaboration with a successful eCommerce platform. The goal is to enable a **Buy Now, Pay Later** service that allows customers to purchase products on credit if they qualify.

## Business Need 💼

Bati Bank recognizes the growing demand for flexible payment solutions and aims to provide customers with the ability to buy products on credit. This requires developing a robust **credit scoring model** to assess the creditworthiness of potential borrowers. The model will utilize data from customer transactions to evaluate risk and determine suitable loan conditions.

## Objectives 🎯

1. Define a proxy variable to categorize users as **high risk** (bad) or **low risk** (good).  
2. Select observable features that are strong predictors of the defined **default variable**.  
3. Develop a model that assigns **risk probabilities** for new customers.  
4. Develop a model that assigns **credit scores** based on risk probability estimates.  
5. Predict the optimal **loan amount** and **duration** for customers.  

## Data and Features 📂

The data for this project is sourced from the **Xente Challenge** on Kaggle. The dataset includes the following fields:

- `TransactionId`: Unique transaction identifier.  
- `BatchId`: Unique batch number for processing.  
- `AccountId`: Unique customer identifier on the platform.  
- `SubscriptionId`: Unique identifier for customer subscriptions.  
- `CustomerId`: Unique customer identifier.  
- `CurrencyCode`: Currency of the transaction.  
- `CountryCode`: Geographical code of the customer's country.  
- `ProviderId`: Source provider of the purchased item.  
- `ProductId`: Name of the purchased item.  
- `ProductCategory`: Broader categories for products.  
- `ChannelId`: Identifies the transaction channel (e.g., web, Android, iOS).  
- `Amount`: Transaction value.  
- `Value`: Absolute value of the transaction.  
- `TransactionStartTime`: Timestamp of the transaction.  
- `PricingStrategy`: Category of pricing structure.  
- `FraudResult`: Fraud status (1 for yes, 0 for no).  

## Folder Structure 📁

```plaintext
📦 root
┣ 📂 .github/workflows
┃ ┗ 📜 ci-cd.yml
┣ 📂 data
┃ ┣ 📜 Xente_Variable_Definitions.csv
┃ ┣ 📜 Xente_Variable_Definitions.xlsx
┃ ┣ 📜 data.csv
┃ ┗ 📜 data.xlsx
┣ 📂 notebooks
┃ ┣ 📂 model
┃ ┃ ┣ 📜 Tuned_XGBoost_model.pkl
┃ ┃ ┣ 📜 Tuned_random_forest_model.pkl
┃ ┃ ┣ 📜 adaboost_model.pkl
┃ ┃ ┣ 📜 decision_tree_model.pkl
┃ ┃ ┣ 📜 logistic_regression_model.pkl
┃ ┃ ┣ 📜 random_forest_model.pkl
┃ ┃ ┗ 📜 xgboost_model.pkl
┃ ┣ 📜 Credit_score_classification_model.ipynb
┃ ┣ 📜 credit_score_EDA.ipynb
┃ ┗ 📜 feature_engineering.ipynb
┣ 📂 plots
┃ ┣ 📜 Amount.png
┃ ┣ 📜 ChannelId_vs_FraudResult.png
┃ ┣ 📜 CountryCode.png
┃ ┣ 📜 Prediction.jpg
┃ ┣ 📜 PricingStrategy.png
┃ ┣ 📜 RFMS_components.png
┃ ┣ 📜 RFMS_space.png
┃ ┣ 📜 Value.png
┃ ┣ 📜 box_plot_numerical_feature.png
┃ ┣ 📜 categorical_distributions.png
┃ ┣ 📜 correlation.png
┃ ┣ 📜 distribution_RFMS.png
┃ ┣ 📜 numerical_histograms.png
┃ ┣ 📜 outlier.png
┃ ┗ 📜 rel_bet_numerical_feature.png
┣ 📂 scripts
┃ ┣ 📜 __init__.py
┃ ┗ 📜 main.py
┣ 📂 src
┃ ┣ 📂 pycache
┃ ┣ 📜 __init__.py
┃ ┣ 📜 eda.py
┃ ┣ 📜 feature_engineering.py
┃ ┣ 📜 load_data.py
┃ ┣ 📜 model_evaluation.py
┃ ┣ 📜 modeling.py
┃ ┣ 📜 train_test_split.py
┃ ┗ 📜 woe_binning.py
┣ 📂 tests
┃ ┣ 📂 pycache
┃ ┣ 📜 __init__.py
┃ ┣ 📜 test_eda.py
┃ ┣ 📜 test_feature_engineering.py
┃ ┣ 📜 test_load_data.py
┃ ┣ 📜 test_model_evaluation.py
┃ ┣ 📜 test_modeling.py
┃ ┗ 📜 test_woe_binning.py
┣ 📂 web-api
┃ ┣ 📂 static/css
┃ ┃ ┣ 📜 output.css
┃ ┃ ┗ 📜 tailwind.css
┃ ┣ 📂 templates
┃ ┃ ┣ 📜 display.html
┃ ┃ ┣ 📜 index.html
┃ ┃ ┗ 📜 result.html
┃ ┣ 📜 README.md
┃ ┣ 📜 app.py
┃ ┣ 📜 data_preprocess.py
┃ ┣ 📜 modeling.py
┃ ┣ 📜 package-lock.json
┃ ┣ 📜 package.json
┃ ┣ 📜 requirements.txt
┃ ┗ 📜 tailwind.config.js
┣ 📜 .gitignore
┣ 📜 Dockerfile
┣ 📜 LICENSE
┣ 📜 README.md
┗ 📜 requirements.txt
```

## How to Use 🚀

1. **Clone the repository:**

```bash
git clone "https://github.com/Getachew0557/Credit-Score-Classifications.git"
```

2. **Navigate to the project directory:**

```bash
cd Credit-Score-Classifications
```

3. **Install dependencies:**

```bash
pip install -r requirements.txt
```

4. **Start the project:**

```bash
python scripts/main.py
```

5. **To forecast store sales, use:**

```bash
python flask-app/app.py
```

- Open your browser and paste `http://127.0.0.1:5000`.
- Fill out the form and submit to see the prediction results. 

## Deploy the Web API on Render 🌐

Step-by-step instructions to deploy to Render:

1. Sign up for a **Render account** and connect it to your **GitHub repository**.
2. Create a new **web service** by selecting your Credit-Score-Classifications repository.
3. Configure the service settings:
   - Select **Python** as the language.
   - Set **Start Command** to:

```bash
python flask-app/app.py
```

4. Deploy the app and get the live **URL**.
5. Access the deployed app by visiting the **Render URL**: [https://credit-score-classifications-1.onrender.com/](https://credit-score-classifications-1.onrender.com/)

For instructions on setting up and deploying the web API, see the [Web API Deployment Guide](web-api/README.md).

## Results 📈

Below is an example of the **credit score and risk modeling prediction** visualization generated by the project:

![Prediction](notebooks/plots/Predction.jpg)

## Contributing 🤝

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request. 

## Contact Information 📧

- **Name**: Yonas Bogale
- GitHub: [jonnahjr](https://github.com/jonnahjr)
- Email: [jonasjjonas14@gmail.com](mailto:jonasjjonas14@gmail.com)
- LinkedIn: [yonas-bogale](https://www.linkedin.com/in/yonas-bogale)

## License 📜

This project is licensed under the **Apache License 2.0**. See the [LICENSE](LICENSE) file for more details.
```
